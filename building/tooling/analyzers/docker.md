# Docker

Our Analyzers are deployed as Docker images.

Please read the [general tooling Docker information](/docs/building/tooling/docker) to familiarize yourself with how these work.

When we run the Analyzer's container we execute a `run.sh` script.
To ensure this works properly the following rules must be followed:

- The working directory should be `/opt/analyzer`.
- There should be a `/opt/analyzer/bin/run.sh` script that can be called with 3 parameters:
  the `exercise slug`, the path to the `solution folder`, and the path to the `output folder`.
  For more information see [The Interface](/docs/building/tooling/analyzers/interface).
