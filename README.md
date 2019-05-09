# DeepMPLS: Fast Analysis of MPLS Configurations Using Deep Learning

This repository contains the dataset used for the paper _"DeepMPLS: Fast Analysis of MPLS Configurations Using Deep Learning"_ publish at the [IFIP Networking 2019](https://networking.ifip.org/2019/) conference. We refer to the paper for a full explanation of the methodology used for generating the dataset.

## Reading the dataset

This dataset is based on the networks from the [topology-zoo dataset](http://www.topology-zoo.org/).
The repository contains two types of files:

- Network description files, stored as a `tar.gz` archive, containing the topologies and the MPLS rules in XML format. The XML format can be processed using [P-Rex](https://github.com/P-RexMPLS/P-Rex).
- Queries files in compressed JSON format.

The matching between network descriptions and queries files is done via the filenames (see example below).

The `dataset/qpred` folder corresponds to the _Satisfiability_ and _Routing_ tasks in the paper, and the `dataset/cpred` folder corresponds to the _Partial synthesis_ task.

### Example query in the JSON files

In `dataset/cpred/topology-zoo/Arpanet196912.queries.json.gz`, the first query is:

```json
{
  "query": "<11> SRI .* UCLA <> 0",
  "query_result": true,
  "network": "s1p49"
}
```

This query corresponds to the network described by the `s1p49/topo.xml` and `s1p49/routing.xml` files from the archive `dataset/cpred/topology-zoo/Arpanet196912.xmls.tgz`.

## Citation

If you use this dataset for your research, please include the following reference in any resulting publication:

```bibtex
@inproceedings{GeyerSchmid_Networking2019,
	author    = {Geyer, Fabien and Schmid, Stefan},
	title     = {{DeepMPLS}: Fast Analysis of MPLS Configurations Using Deep Learning},
	booktitle = {Proceedings of the 18th IFIP Networking Conference},
	year      = {2019},
	month     = mai,
	address   = {Warsaw, Poland},
}
```