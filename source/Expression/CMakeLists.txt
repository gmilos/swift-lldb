add_lldb_library(lldbExpression
  DiagnosticManager.cpp
  DWARFExpression.cpp
  Expression.cpp
  ExpressionSourceCode.cpp
  ExpressionVariable.cpp
  FunctionCaller.cpp
  IRDynamicChecks.cpp
  IRExecutionUnit.cpp
  IRInterpreter.cpp
  IRMemoryMap.cpp
  LLVMUserExpression.cpp
  Materializer.cpp
  REPL.cpp
  UserExpression.cpp
  UtilityFunction.cpp
  )

if(NOT LLDB_BUILT_STANDALONE)
  add_dependencies(lldbExpression intrinsics_gen)
endif()
