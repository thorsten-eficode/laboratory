# dagger

## references

- [dagger](https://www.dagger.io/)
- [dagger docs](https://docs.dagger.io/)
- [dagger @ Github](https://github.com/dagger/dagger)
- [cue](https://cuelang.org)
- [cue docs](https://cuelang.org/docs/)
- [cue @ Github](https://github.com/cuelang/cue)

## cue

> CUE is an open-source data validation language and inference engine with its roots in logic programming. Although the language is not a general-purpose programming language, it has many applications, such as data validation, data templating, configuration, querying, code generation and even scripting. The inference engine can be used to validate data in code or to include it as part of a code generation pipeline.

CUE is particularly well-suited for cases where CUE constraints are combined from different sources:
- Data validation: different departments or groups can each define their own constraints to apply to the same set of data.
- Code extraction and generation: extract CUE definitions from multiple sources (Go code, Protobuf), combine them into a single definition, and use that to generate definitions in another format (e.g. OpenAPI).
- Configuration: values can be combined from different sources without one having to import the other.

CUE does not distinguish between values and types. This is a powerful notion that allows CUE to define ultra-detailed constraints, but it also simplifies things considerably.

```json
largeCapital: {
  name:    string
  pop:     >5M
  capital: true
}
```

### Usage

Convert `cue` to different data formats:

```bash
# defautl output format:
$ cue export examples/001-cue-export.cue
{
    "x": 21.99,
    "y": -10,
    "s": "some string"
}
# output as yaml
$ cue export examples/001-cue-export.cue --out=yaml
x: 21.99
y: -10
s: some string
```

