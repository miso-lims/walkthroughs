<a name="index-distance-simple" href="#">top</a>

# 2. Checking Index Distance

When you run multiple libraries in a sequencing lane or partition, known as multiplexing,
indices are used to identify the individual libraries and demultiplex (separate) the data
afterwards. If two or more libraries in the pool have identical or near-identical indices,
demultiplexing may be more difficult or even impossible. The Index Distance tool can help
you identify indices which may be inadvisable to multiplex together.

1. In the _Tools_ menu on the left, click _Index Distance_. This will take you to the
   Index Distance Tool.
1. Copy and paste the following index sequences into the box on the left:

   ```
   AAAAAAAA
   AAAAAACC
   CCAAAACC
   AAAAAAAA
   ```
   
1. Click _Calculate_. The results pane will show you that there is a duplicate (AAAAAAAA),
   and that two of the sequences are a near match, only differing by 2 bases. (AAAAAAAA and
   CAAAAAAA).

<a name="index-distance-length" href="#">top</a>

# 3. Checking Indices of Different Length

When indices are of different lengths, only the length of the shorter index should be
considered. Click _Clear_ to reset the form and enter the following index sequences.

```
AAAAAA
AAAAAACC
GGAAAATT
GGGAAA
```

Click _Calculate_ and you'll see in the results that when comparing a 6-base index to an
8-base index, only the first 6 bases are compared. Because of this, 'AAAAAA' and 'AAAAAACC'
are considered duplicates, and the other two sequences are considered near-matches with only
a 1-base difference.

<a name="index-distance-dual" href="#">top</a>

# 4. Checking Dual-Index Sequences

With dual indices, it isn't a problem if multiple libraries have one of the same index
sequences, as long as the other index is different. It is the combination of both indices
that must be unique. You can compare dual-index sequences by entering both indices together
as one. For example, take the following indices:

| Index 1 | Index 2 |
| AAAAAA | CCCCCC |
| AAAAAA | TTTTTT |
| GAAAAA | CCCCCC |

Click _Clear_ to reset the form and enter the combined sequences into the Index Distance
Tool:

```
AAAAAACCCCCC
AAAAAATTTTTT
GAAAAACCCCCC
```

Click _Calculate_. Notice that the first two sequences are not considered duplicates even
though index 1 is the exact same. Only the first and third sequences are considered near
matches.

<a name="index-distance-miso" href="#">top</a>

# 5. Selecting Indices from MISO

Rather than copying them from another source, or typing in the index sequences yourself,
you can also choose indices from MISO to compare.

1. Click _Clear_ to reset the form.
1. From the _Indices_ list below the form, select any 5 indices.
1. Click _Add_ from the toolbar. The sequences will appear in the _Indices_ box of the
   tool above.
1. Click _Calculate_ to check for duplicates or near matches.

