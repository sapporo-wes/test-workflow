# Sapporo and Yevis test workflow

[![Apache License](https://img.shields.io/badge/license-Apache%202.0-orange.svg?style=flat&color=important)](http://www.apache.org/licenses/LICENSE-2.0)

This repository summarizes examples and results of actual widely used workflows executed with [Sapporo](https://github.com/sapporo-wes/sapporo) and [Yevis](https://github.com/suecharo/yevis-cli).

The workflows that were verified are as follows:

- [`gatk-workflows/gatk4-data-processing`](https://github.com/gatk-workflows/gatk4-data-processing)
- [`nf-core/rnaseq`](https://github.com/nf-core/rnaseq)
- [`ddbj/human-reseq`](https://github.com/ddbj/human-reseq)

## Verification environment

- Ubuntu: `20.04`
- Docker: `20.10.15`
- sapporo-service: `1.2.1`
- yevis-cli: `0.3.2`

## Execution methods and results

We use [Yevis](https://github.com/suecharo/yevis-cli) as the execution runner for [Sapporo](https://github.com/sapporo-wes/sapporo).
Yevis reads a file called `yevis-metadata`, which describes workflow metadata and test execution methods, and generates an workflow execution request (i.e. a POST request to `/runs` in Sapporo) to Sapporo.
Therefore, as execution methods, we have prepared execution commands using Yevis and `yevis-metadata` files.

In addition, as execution results, we uploaded `run_dir`, the result of sapporo's execution, to [Zenodo](https://zenodo.org/).
The `run_dir` contains various workflow provenances such as input/output files, execution logs, and run request.

### `gatk-workflows/gatk4-data-processing`

### `nf-core/rnaseq`

### `ddbj/human-reseq`

## License

[Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0).
See the [LICENSE](https://github.com/sapporo-wes/test-workflow/blob/main/LICENSE).
