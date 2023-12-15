# Howareyou

# This workflow uses actions that are not certified by GitHub.
# They are provided by a third-party and are governed by
# separate terms of service, privacy policy, and support
# documentation.

# This workflow will install Deno then run `deno lint` and `deno test`.
# For more information see: https://github.com/denoland/setup-deno

name: Deno

on:
  push:
    branches: ["main"]
  pull_request:
    branches: ["main"]

permissions:
  contents: read

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
      - name: Setup repo
        uses: actions/checkout@v3

      - name: Setup Deno
        # uses: denoland/setup-deno@v1
        uses: denoland/setup-deno@61fe2df320078202e33d7d5ad347e7dcfa0e8f31  # v1.1.2
        with:
          deno-version: v1.x

      # Uncomment this step to verify the use of 'deno fmt' on each commit.
      # - name: Verify formatting
      #   run: deno fmt --check

      - name: Run linter
        run: deno lint

      - name: Run tests
        run: deno test -A
![IMG_20230808_013511-01](https://github.com/Termuxmasud404/Howareyou/assets/118968969/36edf9f5-1a06-488a-a481-6eee1519a367)


steps:
  - name: Setup repo
    uses: actions/checkout@v3

  - name: Setup Deno
    # uses: denoland/setup-deno@v1
    uses: denoland/setup-deno@61fe2df320078202e33d7d5ad347e7dcfa0e8f31  # v1.1.2
    with:
      deno-version: v1.x

  # Uncomment this step to verify the use of 'deno fmt' on each commit.
  # - name: Verify formatting
  #   run: deno fmt --check

  - name: Run linter
    run: deno lint

  - name: Run tests
    run: deno test -A


Thanks 
  🥀🥀
