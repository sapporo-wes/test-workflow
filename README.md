# Sapporo test workflow

[![Apache License](https://img.shields.io/badge/license-Apache%202.0-orange.svg?style=flat&color=important)](http://www.apache.org/licenses/LICENSE-2.0)
[![DOI](https://zenodo.org/badge/490141598.svg)](https://zenodo.org/badge/latestdoi/490141598)

This repository summarizes examples and results of actual widely used workflows executed with [Sapporo](https://github.com/sapporo-wes/sapporo) and [Yevis](https://github.com/ddbj/yevis-cli).

The workflows that were verified are as follows:

- [`broadinstitute/gatk/MitochondriaPipeline`](https://dockstore.org/workflows/github.com/broadinstitute/gatk/MitochondriaPipeline:master?tab=info)
- [`nf-core/rnaseq`](https://github.com/nf-core/rnaseq)
- [`biosciencedbc/jga-analysis - per-sample workflow`](https://github.com/biosciencedbc/jga-analysis/blob/main/per-sample/Workflows/per-sample.cwl)

## Verification environment

- Ubuntu: `20.04`
- Docker: `20.10.15`
- sapporo-service: `1.2.3`
- yevis-cli: `0.3.3`

## Execution methods and results

We use [Yevis](https://github.com/ddbj/yevis-cli) as the execution runner for [Sapporo](https://github.com/sapporo-wes/sapporo).
Yevis reads a file called `yevis-metadata`, which describes workflow metadata and test execution methods, and generates a workflow execution request to Sapporo. (i.e., a POST request to `/runs` in Sapporo)
Therefore, as execution methods, we have prepared execution commands using Yevis and `yevis-metadata` files.

In addition, as execution results, we uploaded `run_dir`, the result of Sapporo's execution, to [Zenodo](https://zenodo.org/).
The `run_dir` contains various workflow provenances such as input/output files, execution logs, and run requests.

### `broadinstitute/gatk/MitochondriaPipeline`

The execution method is as below:

```bash
yevis test https://raw.githubusercontent.com/sapporo-wes/test-workflow/main/yevis-metadata_gatk-workflows_mitochondria-pipeline.yml
```

The execution results are uploaded to [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.6535083.svg)](https://doi.org/10.5281/zenodo.6535083).

### `nf-core/rnaseq`

The execution method is as below:

```bash
yevis test https://raw.githubusercontent.com/sapporo-wes/test-workflow/main/yevis-metadata_nf-core_rnaseq.yml
```

The execution results are uploaded to [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.6534202.svg)](https://doi.org/10.5281/zenodo.6534202).

### `biosciencedbc/jga-analysis - per-sample workflow`

The execution method is as below:

```bash
yevis test https://raw.githubusercontent.com/sapporo-wes/test-workflow/main/yevis-metadata_jga-workflow_per-sample.yml
```

The execution results are uploaded to [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.6612737.svg)](https://doi.org/10.5281/zenodo.6612737).

## License

[Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0).
See the [LICENSE](https://github.com/sapporo-wes/test-workflow/blob/main/LICENSE).
