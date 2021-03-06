cmake_minimum_required(VERSION 2.8.8)

project(SMPI-proxy-apps)

INCLUDE(CTest)
ENABLE_TESTING()

# Trinity-Nersc benchmarks
ADD_TEST(Trinity_MDTest  bin/Trinity_MDTest.sh)
ADD_TEST(Trinity_stream  bin/Trinity_stream.sh)
#ADD_TEST(Trinity_PSNAP   bin/Trinity_PSNAP.sh) # This test is very long. Comment it for now
ADD_TEST(Trinity_SMB     bin/Trinity_SMB.sh)
ADD_TEST(Trinity_ZiaTest bin/Trinity_ZiaTest.sh)
ADD_TEST(Trinity_MPIMemu bin/Trinity_MPIMemu.sh)
ADD_TEST(Trinity_OMB_MPI_pt2pt bin/Trinity_OMB_MPI_pt2pt.sh)
ADD_TEST(Trinity_OMB_MPI_one-sided bin/Trinity_OMB_MPI_one-sided.sh)
ADD_TEST(Trinity_OMB_MPI_collective bin/Trinity_OMB_MPI_collective.sh)
ADD_TEST(Trinity_GTC     bin/Trinity_GTC.sh)
ADD_TEST(Trinity_MiniFE  bin/Trinity_MiniFE.sh)

# Coral benchamrks 
ADD_TEST(Coral_AMG2013    bin/Coral_AMG2013.sh)
ADD_TEST(Coral_HACC_IO    bin/Coral_HACC_IO.sh)
ADD_TEST(Coral_KMI_HASH    bin/Coral_KMI_HASH.sh)

# Mantevo benchmarks 
ADD_TEST(Mantevo_MiniSMAC2D bin/Mantevo_MiniSMAC2D.sh)
ADD_TEST(Mantevo_MiniEF     bin/Mantevo_MiniEF.sh)
ADD_TEST(Mantevo_MiniXyce   bin/Mantevo_MiniXyce.sh)
ADD_TEST(Mantevo_HPCCG      bin/Mantevo_HPCCG.sh)
ADD_TEST(Mantevo_MiniAMR    bin/Mantevo_MiniAMR.sh)

# CodeVault benchmarks
ADD_TEST(CodeVault_PreExec  bin/CodeVault_PreExec.sh)
ADD_TEST(CodeVault_IntegralBasic  bin/CodeVault_IntegralBasic.sh)
ADD_TEST(CodeVault_Pi             bin/CodeVault_Pi.sh)
ADD_TEST(CodeVault_Prng           bin/CodeVault_Prng.sh)
ADD_TEST(CodeVault_DynSparse      bin/CodeVault_DynSparse.sh)
ADD_TEST(CodeVault_parallelio      bin/CodeVault_parallelio.sh)

# ECP benchmarks 
ADD_TEST(ECP_CoMD      bin/ECP_CoMD.sh)
ADD_TEST(ECP_AMG       bin/ECP_AMG.sh)


