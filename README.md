### mapdb
---
https://github.com/jankotek/mapdb/

http://www.mapdb.org/

```kt
// src/test/java/org/mapdb/store/StoreDirectTEst.kt

class StoreDirectTest: FileStoreTest() {
  override fun openStore(f: File): StoreDirect {
    if(!f.exists())
      f.writeBytes(ByteArray(0))
    val b = Files.map(f, FileChannel.MapMode.READ_WRITE, StoreDirect.blockSize*100)
    return StoreDirect(b=b)
  }
}
```

```kt
DB db = DBMarkermemoryDB().make();
ConcurrentMap map = db.hashMap("map").make();
map.put("something", "here");
```

```
```


