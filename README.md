# *bsc-snapshots*


*\> [geth-snapshots](#geth-snapshots)*

*\> [erigon-snapshots](#erigon-snapshots)*


## geth-snapshots


> Database uses [geth(v1.1.11)](https://github.com/bnb-chain/bsc/releases/tag/v1.1.11) for sync


### download

<!-- begin_geth -->

!!! from block [19092402](https://bscscan.com/block/19092402)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/geth.19092402.tar.lz4 -o geth.tar.lz4
```


### checksum


!!! db size 534.81 gb, 546.38 gb after decompression
```bash
> openssl sha256 geth.tar.lz4
SHA256(geth.tar.lz4)= 9b588f01a54acce86839afc5c581bbbe35f44569c8a932c91db840782d968281
```

<!-- end_geth -->

### uncompress


running a script: _`lz4 -cd geth.tar.lz4 | tar xf -`_


### flags


```bash
--txlookuplimit=0 --diffsync --syncmode=snap
```


## erigon-snapshots


> Database uses [erigon(v2022.06.06)](https://github.com/ledgerwatch/erigon/releases/tag/v2022.06.06) for sync


### download

<!-- begin_erigon -->

!!! from block [19087958](https://bscscan.com/block/19087958)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/erigon.19087958.tar.lz4 -o erigon.tar.lz4
```


### checksum


!!! db size 735.66 gb, 1039.24 gb after decompression
```bash
> openssl sha256 erigon.tar.lz4
SHA256(erigon.tar.lz4)= 76ce5d5de200e89eca65abb1a505c0563c6e3f0c6d98d7f91e53345f735e7094
```

<!-- end_erigon -->

### uncompress


running a script: _`lz4 -cd erigon.tar.lz4 | tar xf -`_


### flags


```bash
--chain=bsc --prune= --prune.h.older=5000 --prune.r.older=5000 --prune.t.older=5000 --prune.c.older=5000 --db.pagesize=16k
```
