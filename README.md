guix_missing

Sometimes files are missing when Guix building, 
more often when with `--no-substitutes`.

This can result in:
```bash
building /gnu/store/3fmrgvx8aajw7vys3h8ng5fk42ch5878-libgpg-error-1.45.tar.bz2.drv...
/sha256 hash mismatch for /gnu/store/p0x73jkcv1n5b5r9xhvbcw5nkzgh49rj-libgpg-error-1.45.tar.bz2:
  expected hash: 09haz1kk48b8q0hd58g98whylah0fp121yfgjms7pzsbzgj8w3sp
  actual hash:   1x98ffbgfly8mkb6c9swzg0lp9alrvxirjypl03aqgn8y264c0p8
hash mismatch for store item '/gnu/store/p0x73jkcv1n5b5r9xhvbcw5nkzgh49rj-libgpg-error-1.45.tar.bz2'
build of /gnu/store/3fmrgvx8aajw7vys3h8ng5fk42ch5878-libgpg-error-1.45.tar.bz2.drv failed
View build log at '/var/log/guix/drvs/3f/mrgvx8aajw7vys3h8ng5fk42ch5878-libgpg-error-1.45.tar.bz2.drv.gz'.
```

Generally these errors are not actually packages changed in place,
but missing packages or broken mirrors.

If you run into a missing package, you can do:
```bash
guix download https://github.com/fanquake/guix_missing/raw/refs/heads/main/the_missing_file.some.extension
```
