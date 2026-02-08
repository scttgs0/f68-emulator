ifeq ($(OS),Windows_NT)
include ..\documents\common.make
else
include ../documents/common.make
endif

SOURCE=FoenixMCP$(S)src$(S)

all:rom

rom	:
	make -C $(SOURCE) UNIT=a2560k MEMORY=flash 
	$(CCOPY) $(SOURCE)foenixmcp.s68 ..$(S)emulator$(S)a2560k.rom

clean:
	make -C $(SOURCE) clean

#
# 		FoenixMCP is a clone of the repository main branch.
# 		
#		The text_init() at 301 of foenixmcp.c has been uncommented so that
# 		it switches back to text mode at the end.
#
#		Also text_init() has been changed so that chan_a is
#		now set up to access Vicky III *B* (lines 215-248, text_screen_iii.c)
#		by force (subtle changes didn't work !)
#
