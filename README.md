# Brucon 0x0D 2021

# Automating Binary Analysis with Ghidra's P-Code

# Video
https://www.youtube.com/watch?v=Qift_6-3y3A&list=PLtb1FJdVWjUeYggPpHRvI7yGAsMpmIwO1

# Abstract

“Ghidra is a software reverse engineering (SRE) framework created and maintained by the National Security Agency Research Directorate“ (https://github.com/NationalSecurityAgency/ghidra). It provides a great free and capable alternative to IDA Pro and Binary Ninja for manual static binary analysis. A lesser-known fact is, that Ghidra also provides a great API and an even better SDK for writing Ghidra scripts. The API can be used to quickly script tasks in your reversing work, however, the SDK allows access to everything that is under the hood. This allows you to write scripts that can do anything that is possible with Ghidra. And with that you are not limited anymore to simple scripts, you can write full automated binary analysis tools that use Ghidra in headless mode.

Another lesser-known feature of Ghidra is its intermediate language called P-Code. P-Code lies between the assembly code and the decompiled code that the Ghidra UI shows. It is a register transfer language, it translates every individual processor instruction to a sequence of P-Code operations that describes the processor instruction, including all side effects, such as setting a flag.

In this talk, we are going to focus on the combination of these two features and start building binary analysis tools using Ghidra P-Code. This setup has some significant benefits. Just to mention one, if you are only working with P-Code and never look at the assembly, then your script will be architecture-independent and will support all architecture that is supported by the Ghidra decompiler. Another significant benefit is that Ghidra is free and open source. That allows you to deploy your tool more freely without worrying about licensing issues and gives you the possibility to dig deep in Ghidra’s source code to understand how different classes work.

We will first familiarize ourselves with P-Code. Understand how it works and how it looks like when we are accessing it through the SDK. Then start building simple scripts to see P-Code used in automation. With these, we will work our way up to a more complex scenario.

Independently from what your favorite disassembler is, it is worth looking at Ghidra because it holds some interesting features that can help you in your next binary analysis project.