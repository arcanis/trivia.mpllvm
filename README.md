trivia.mpllvm
=============

Metaprogramming type resolver for LLVM

- `llvm::Type * mpllvm::get< T >( llvm::LLVMContext & llvmContext )`

  Returns the corresponding LLVM type of `T`.

  Ex : `llvm::Type * foo = mpllvm::get< int >( llvmContext );`

- `llvm::Type * mpllvm::deduce( llvm::LLVMContext & llvmContext, T const & t )`

  Returns the corresponding LLVM type of the value `t`.

  Ex : `llvm::Type * foo = mpllvm::deduce( llvmContext, &malloc );`

- `llvm::StructType * mpllvm::craft< T... >( llvm::LLVMContext & llvmContext, bool isPacked = false )`

  Returns a LLVM structure type whose each field is one of the template parameter.

  Ex : `llvm::StructType * foo = mpllvm::craft< int, int >( llvmContext );`
