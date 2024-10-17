# Introduction
As part of my work-study program as a reverse engineer, I'm in charge of analyzing the various layers of obfuscation in compiled code through the interfaces of the Tigress and OLLVM compilers. The final rendering is a GUI overlay for three types of decompiler (IDA Pro, Ghidra, and Binary Ninja) to enable real-time code clean-up with a native C plugin or an external Python script (which I'll have to justify with a benchmark).

## Obfuscation Overview
Software obfuscation is a method to make programs more difficult to reverse engineer. There are multiple reasons why this is done, such as protecting intellectual property, defense in depth, or hiding bugs. No matter the reason, there are multiple ways to make the software more difficult to understand, from fully manual modifications to advanced commercial obfuscation frameworks.

Before trying to de-obfuscate anything and everything, you need to understand how obfuscation works, its different application and abstraction layers, and above all, how it works with LLVM and Tigress.

For a detailed analysis, please refer to the following dedicated READMEs:

- [Obfuscation In General](src/README.md)
- [Tigress Options](src/tigress/options.md)
  - [Tigress Testing](src/tigress/README.md)
- [OLLVM Analysis](src/ollvm/README.md)
- [Benchmarks](benchs/README.md)

Go through each README for an in-depth look at the various aspects and techniques of obfuscation we are analyzing.

## Obfuscation In General
The detailed analysis of general obfuscation techniques is documented [here](src/README.md).

## Tigress Testing
The detailed analysis of Tigress obfuscation techniques is documented [here](src/tigress/).

> [!IMPORTANT]
> In the first demo version I mainly used Ghidra for analyses, and in the second one i used IDA Pro 9.0

## OLLVM Analysis
The detailed analysis of OLLVM obfuscation techniques is documented [here](src/ollvm/README.md).<br>
For the moment, it's more about O-MVLL.... cause ollvm is too old.

## Benchmarks
To justify the use of a native C plugin versus an external Python script, benchmark details are provided [here](benchs/README.md).

---
> [!NOTE]
> Feel free to navigate through the links to get a more comprehensive understanding of each section.<br>
> The "professional" version of the analysis is present in the [notebooks](notebooks/). <br>
> The personal version is all the source. I suggest to read the professional one, since, it's more organized.<br>

<br>

You can site this analyse using the following Bibtex entry:
```latex
@misc{reverse_engineering_analysis,
  author       = {Alexis Daugé (aldauge)},
  title        = {Analyses of Obfuscation Generated by OLLVM and Tigress.},
  year         = {2024},
  howpublished = {Work-Study Program Report},
  url          = {https://github.com/ringiclub/obfuscation},
}
```
---

## References

- Obfuscator-LLVM. Available at: [https://github.com/obfuscator-llvm/obfuscator](https://github.com/obfuscator-llvm/obfuscator)
- Jonathan Salwan, *Tigress Protection*. Available at: [https://github.com/JonathanSalwan/Tigress_protection](https://github.com/JonathanSalwan/Tigress_protection)
- Tigress Obfuscation Tool. Available at: [https://tigress.wtf/](https://tigress.wtf/)
- Zeta Two, *Security Fest 2019 - Obfuscation Slides*. Available at: [https://zeta-two.com/assets/other/securityfest19-obfuscation-slides-errata.pdf](https://zeta-two.com/assets/other/securityfest19-obfuscation-slides-errata.pdf)
- Imperva, *Data Obfuscation*. Available at: [https://www.imperva.com/learn/data-security/data-obfuscation/](https://www.imperva.com/learn/data-security/data-obfuscation/)
- Jonathan Salwan, *Obfuscation-related PhD Thesis*. Available at: [https://www.cs.ox.ac.uk/files/2892/thesis.pdf](https://www.cs.ox.ac.uk/files/2892/thesis.pdf)
- OMVLL, *Obfuscator*. Available at: [https://obfuscator.re/omvll/introduction/](https://obfuscator.re/omvll/introduction/)
- YouTube, *Advanced Obfuscation Techniques - Jonathan Salwan*. Available at: [https://www.youtube.com/watch?v=bQpPdT7RDqQ](https://www.youtube.com/watch?v=bQpPdT7RDqQ)
