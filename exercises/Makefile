# -*- Makefile -*-

## Find all RMD files beginning with "exercise":
QMDS := $(wildcard exercise*.qmd)

## Strip the file extension off the located RMD files:
NAMES := $(QMDS:%.qmd=%)

all: ${NAMES}

## Rule to compile both the RMD files with and without solutions: 
%: %.qmd
	Rscript --vanilla render.R $@ TRUE
	Rscript --vanilla render.R $@ FALSE

clean:
	rm mammalsleep.txt practical3.RData sleepdata.RData sleepdata.rds
