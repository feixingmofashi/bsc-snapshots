
<!-- begin_TYPE -->

!!! from block [NUMBER](https://bscscan.com/block/NUMBER)

#### pipeline download and extract
> skip checksum & uncompress if you used pipeline
```bash
wget https://snapshots.48.club/geth.TYPE.NUMBER.tar.lz4 -O - | lz4 -cd | tar xf -
```

#### multithreaded download

```bash
aria2c -s4 -x4 -k1024M https://snapshots.48.club/geth.TYPE.NUMBER.tar.lz4 -o TYPE.tar.lz4
```


### checksum

!!! db size ZIP_SIZE gb, FULL_SIZE gb after decompression
```bash
> openssl sha256 TYPE.tar.lz4
SHA256(TYPE.tar.lz4)= CHECKSUM
```

<!-- end_TYPE -->
