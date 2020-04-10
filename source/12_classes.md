# Data structure in Authentication1

## Classes used in code

There are mainly 2 classes used widely in `authentication_1`. I have named them `hlf_maybe_class_1_10073ed8` and `AutoClass2`. 

### `hlf_maybe_class_1_10073ed8`

The class `hlf_maybe_class_1_10073ed8` has at least 240 bytes. However, this is not verified as some fields might only take up a byte and there is no clue of how many fields are there in the class. The constructor of the class is believed to be at `10012430`. This function was called when the DLL was loaded, with the parameter being the address `10073ed8`. This function is a *thiscall* and conatins mostly initialisation of variables in the parameter, as well as memory allocations. Therefore, it is reasonable to deduce that the function `10012430` is a constructor to the class `10073ed8`. 

<!-- ![Snippet of the constructor with `this` points to `10073ed8` \label{hahhaha}](source/img/snippet_ctor_10073ed8.png) -->

\begin{figure}[h!]
  \includegraphics[]{source/img/snippet_ctor_10073ed8.png}
  \caption{hahahahah}
  \label{fig:boat1}
\end{figure}

\ref{fig:boat1}
\vfill

From brief investigation throughout the code, I have deduced several members of the class.

| Offset | Type             | Meaning                                                            |
|:------:|:----------------:|:------------------------------------------------------------------:|
| 0x4    | `void*`          | A pointer pointing to a class or array                             |
| 0x38   | `bool` or `uint` | Value equals 1 if the communication port has opened, 0 otherwise   |
| 0xc0   | `bool` or `uint` | Value equals 1 if library and plugins are initialised, 0 otherwise |
| 0xc1   | `bool` or `uint` | Same as `0xc0`                                                     |
| 0xF0   | `byte`           | Equals 1 (reason and usage not found)                              |



### `AutoClass2`

oaisdfoisajdfoisjdafioasdf
jasodifoaisdjf
oiasdf
oasjdfiasdfiasjodf
ajsidf
oaijdf
oaisdjf
osaidjfoidsjfoisjdfoisjdf
asdjf
oaisjdf
oaisdjf
oasidjf
aodsijf
asodijfosdifjosidfjoisf
