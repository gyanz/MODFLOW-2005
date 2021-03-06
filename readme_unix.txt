README.TXT


                       MODFLOW-2005 - Version: 1.12.00
         Three-dimensional finite-difference ground-water flow model


NOTE: Any use of trade, product or firm names is for descriptive purposes 
      only and does not imply endorsement by the U.S. Government.

This version of MODFLOW is referred to as MODFLOW-2005 in order to distinguish
it from older versions of the code.  This version of MODFLOW-2005 is packaged
for use on computers using a Unix operating system.  Source and documentation
files are provided, but not an executable file.  Fortran and C compilers are
required to create an executable file.

IMPORTANT: Users should review the file Mf2005.txt for a description of, and
references for, this software. Users should also review the file release.txt,
which describes changes that have been introduced into MODFLOW-2005 with each
official release; these changes may substantially affect users.


The following file is provided for Unix computers:

         MF2005.1_12u.zip

The zipped file contains numerous individual files.  Source files will
be in subdirectory src, and documentation files will be in subdirectory doc.
Some of the documentation files are Portable Document Format (PDF) files.
The PDF files are readable and printable on various computer platforms
using Acrobat Reader from Adobe.  Subdirectory test-run contains data
files for test problems as described in problems.txt.  Subdirectory
test-out contains the listing output files from running the test problems
on a personal computer.

MODFLOW must be compiled before it can be run on a computer.  The
requirements are a Fortran compiler, a compatible C compiler, and the
knowledge of using the compilers.  The C compiler is used for the GMG
solver.  If a compatible C compiler is not available, the GMG solver
can be removed so that only a Fortran compiler is required.  File
nogmg.txt in the src subdirectory contains instructions for
removing GMG from MODFLOW.  An example makefile for compiling is
provided in the make subdirectory, but changes may be required to work
on specific computers.  The USGS cannot provide assistance with
compiling MODFLOW.

Some of the files written by MODFLOW are unformatted files.  The structure
of these files depends on the compiler and options in the Fortran write
statement.  Any program that reads the unformatted files produced by
MODFLOW must be compiled with a compiler that produces programs that
use the same structure for unformatted files.  For example, Zonebudget
and Modpath use unformatted budget files produced by MODFLOW.  Another
example is head files that are generated by one MODFLOW simulation and
used in a following simulation as initial heads.  Both simulations must
be run using an executable version of MODFLOW that uses the same
unformatted file structure.

This issue of unformatted files is described here so that users will
be aware of the possibility of problems caused by unformatted files. 
The source file openspec.inc may require modification before compiling
to cause unformatted files to be written as desired.
