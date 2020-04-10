# Introduction

## Background

FeliCa is a contactless RFID smart card system developed by Sony in Japan. It can be used in several situations such as electronic payments and access control. It was first used in Octopus card system in 1997 in Hong Kong and was successful. People in Hong Kong are still using it for transportation and electronic payments. It was then used in other countries including Singapore, Japan and United States.

## Aims of project

The aim of the project is to analyse the authentication protocol by reverse engineering a function called `authentication_1` in a Dynamic-Link Library (DLL). It contains several function calls with reasonable amount of strings to hint what it is trying to achieve.

## Background

The authentication process of FeliCa has been a mist. In official documents, they only mention FeliCa uses mutual authentication to keep the communication secure and efficient. The transaction process, including encryption and authentication, takes only 0.1 second. ===== Ref{https://www.sony.net/Products/felica/about/scheme.html#scheme03} ===== However, the authentication does not entirely follow open standards. Sony has developed their own standard in terms of secure transaction. ==Ref== This makes researchers difficult to analyse the protocol. 

Fortunately, there is a DLL called `rw.dll`, which perhaps stands for *read/write*. There are 132 exported functions and lots of other private helper functions. Exported functions can be called by name or ordinal after importing the library. Private helper functions can be called as well, but not by name or ordinal but by their offsets. This will be explained in later section. 


## Abbreviations

Common abbreviations are explained here.

| Abbreviation | Meaning              |
|:------------:|:--------------------:|
| DLL          | Dynamic-Link Library |
| RE           | Reverse Engineering  |


<!-- 
To include a reference, add the citation key shown in the references.bib file.
-->

To include a citation to the text, just add the citation key shown in the references.bib file. The style of the citation is determined by the ref_format.csl file. For example, in The Living Sea you can find pictures of the Calypso [@Cousteau1963].
