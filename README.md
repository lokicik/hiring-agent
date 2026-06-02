# hiring-agent contribution fork

This repository is a fork of HackerRank's `hiring-agent`, used for contributing parser robustness improvements and OpenRouter provider support.

## Contribution

I worked on two improvements:

* Fixing / improving resume parsing behavior around structured extraction failures
* Adding OpenRouter support as an additional LLM provider option

The work came from testing the tool against real resumes and hitting validation/parsing issues during PDF extraction, including cases where the extracted basics section failed structured validation.

## Changes

### Parser robustness

Improves handling around resume parsing failures where structured section extraction can fail or produce incomplete fields.

Example issue:

```txt
Basics.name
Field required [type=missing]
```

The goal is to make the extraction flow more resilient when the model response is incomplete, malformed, or does not fully match the expected schema.

### OpenRouter provider support

Adds support for using OpenRouter-hosted models as an LLM provider, making it easier to test the hiring-agent workflow across different model families without changing the core evaluation pipeline.

## Status

Pull request: In Progress
Status: Open

## Upstream

Original repository: [https://github.com/interviewstreet/hiring-agent](https://github.com/interviewstreet/hiring-agent)
