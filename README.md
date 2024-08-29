# Compiladores
Código para la materia Compiladores de [LCC](https://dcc.fceia.unr.edu.ar), [FCEIA](https://www.fceia.unr.edu.ar), [UNR](https://www.unr.edu.ar).

Para fijar la versión de GHC y de los paquetes se usa la herramienta [stack](https://docs.haskellstack.org/en/stable/README/).

Cómo dependencias se necesita instalar:

- la librería para desarrolladores de ncurses (para compilar [haskeline](https://hackage.haskell.org/package/haskeline)):
- clang	(para compilar a LLVM)
- libgc (garbage collector para C y C++)
```code
sudo apt install libncurses-dev clang libgc-dev
```

Una vez clonado el repositorio hay que instalar el compilador GHC que vamos a usar:
```code
stack setup
stack build
```

Luego se puede ejecutar con:
```code
stack run
```

y se pueden pasar argumentos agregando --
por ejemplo para ver el texto de ayuda
```code
stack run -- -h
```


o cargar el entorno interactivo GHCi
```code
stack ghci

stack ghci src/TypeChecker.hs
```