# Appendix A: One published vector set as an example

Chapter 5 describes four things a project can ship: test vectors, a manifest, a runner and a testing statement.
This appendix names one public project that already ships all four for one record format, so a reader can see what they look like.
It is an illustration, not a recommendation of a tool.

| Role in chapter 5 | In agent-evidence-vectors |
| --- | --- |
| Test vectors | Signed records, each paired with the result a verifier must return, with many that must be rejected |
| Manifest | A file listing every vector with its expected result, pinned by one digest |
| Runner | A command that feeds each vector to a verifier and reports which ones differ from the expected result |
| Testing statement | A short page on what the vectors check and what they leave open |

An integrator whose product embeds a library that verifies signed records pins one release of the vector set in the product's build and points the runner at the library.
When the build fails, the runner names the vector whose result changed.
The integrator records the run in the due diligence record from chapter 3, with the output referenced by its digest.

The vector set is at https://github.com/probityai/agent-evidence-vectors and is installed with `pip install agent-evidence-vectors==0.26.0`.
