include_directories(
  ${LLVM_MAIN_SRC_DIR}/lib/Target/ARM
  ${LLVM_BINARY_DIR}/lib/Target/ARM
  )

set(LLVM_LINK_COMPONENTS
  ARMCodeGen
  ARMDesc
  ARMInfo
  CodeGen
  CodeGenTypes
  Core
  GlobalISel
  MC
  MIRParser
  SelectionDAG
  Support
  Target
  TargetParser
  )

add_llvm_target_unittest(ARMTests
  MachineInstrTest.cpp
  InstSizes.cpp
  )
