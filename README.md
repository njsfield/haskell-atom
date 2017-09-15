# Overview

The [IDE-Haskell](https://atom.io/packages/ide-haskell) atom plugin allows many features in Atom to help improve workflow
when writing Haskell code.

The following steps outline a basic setup; 

Make sure you are using an up to date version of [stack](https://docs.haskellstack.org/en/stable/README/)

1. Install [ide-haskell](https://atom.io/packages/ide-haskell) & [haskell-ghc-mod](https://github.com/DanielG/ghc-mod) plugins in Atom.
2. Run `stack install stylish-haskell`.
3. After the installation, you'll likely see errors outlining the exectuables are not available on PATH. Locate the installed stylish-haskell executables and copy them to `/usr/local/bin`.
4. Run `stack install ghc-mod` (this will install ghc and ghci).
5. (Again, if errors are shown, move ghc & ghci executables to `/usr/local/bin` to be visible on PATH.)
6. In *ide-haskell* settings on Atom, change **Message Display Frontend** setting from *builtin* to *linter* so that linting errors are reported via atoms linter.
7. In *ide-haskell* settings, enable **On Save Prettify (optional)**.

## Linting options

*stylish-haskell* is a shallow formatter. It’s mainly useful for aligning columns for import statements and type signatures.

Alternatively you can use *hindent* as a formatter (`stack install hindent`) and set it in the *ide-haskell* settings in Atom. 
I'd recommend trying both, and reading their documentation for configuration options to decide which is best to use.
- [Hindent](https://github.com/commercialhaskell/hindent)
- [Stylish](https://github.com/jaspervdj/stylish-haskell)
