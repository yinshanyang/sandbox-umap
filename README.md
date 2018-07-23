# `sandbox-umap`

## `embed`

```
usage: embed [-h] [-r ROWS] [-n NEIGHBORS] [--input_dimensions DIMENSIONS]
             [-d DIMENSIONS] [-m MIN_DIST] [--metric METRIC]
             INPUT OUTPUT

UMAP, but with arguments

positional arguments:
  INPUT                 source vector file, the thing that comes out of
                        fastText or word2vec
  OUTPUT                output path

optional arguments:
  -h, --help            show this help message and exit
  -r ROWS, --rows ROWS  number of rows to use (default: 100000)
  -n NEIGHBORS, --neighbors NEIGHBORS
                        number of neighbors, 5 - 50 (default: 15)
  --input_dimensions DIMENSIONS
                        number of dimensions in source word embeddings
                        (default: 300)
  -d DIMENSIONS, --output_dimensions DIMENSIONS
                        number of output dimensions to embed (default: 2)
  -m MIN_DIST, --min MIN_DIST
                        minimum distance, 0.001 - 0.5 (default: 0.1)
  --metric METRIC       distance function, e.g. euclidean, correlation
                        (default: euclidean)
```

### Input (Vectors)

> note: there is no index column, it’s a space-delimited file of the vector values

```
-0.0032 -0.0722  0.0054 ... -0.0151 -0.0035 -0.0059
 0.0089 -0.0051  0.0078 ... -0.0107 -0.0224 -0.0012
 0.005  -0.0114  0.015  ... -0.0015 -0.0138 -0.016
 ...
-0.0008 -0.0075 -0.0023 ... -0.0054 -0.0123 -0.0103
 0.0015 -0.008  -0.008  ...  0.0072 -0.0123  0.0033
 0.0007 -0.0098  0.0038 ...  0.008  -0.011  -0.0024
```

### Output (Projections/Embeddings)

> note: there is no header row, and it’s comma-delimited

```
0,-0.8076544,1.8683653
1,1.2781376,1.6543796
2,-1.3889802,0.4740771
...
7,-1.9511567,3.9544692
8,-2.6282637,3.7856507
9,-0.902199,3.368067
```
