PROJ_NAME = Smart_Firealarm

BUILD_DIR = Build

# All Source code files
SRC = proj_main.c\
src/main.c\
src/Firealarm1.c\
src/Firealarm2.c\
src/Firealarm3.c\



#Object copy to create hexfile
OBJCOPY = avr-objcopy.exe


#Options for HEX file generation
HFLAGS = -j .text -j .data -O ihex

# All header file paths
INC = -I inc

# Find out the OS and configure the variables accordingly
ifdef OS	# All configurations for Windwos OS
   # Delete command 
   RM = del /q
   # Correct the path based on OS
   FixPath = $(subst /,\,$1)
   # Name of the compiler used
   CC = avr-gcc.exe
   # Name of the elf to hex file converter used
   AVR_OBJ_CPY = avr-objcopy.exe
else #All configurations for Linux OS
   ifeq ($(shell uname), Linux)
   	  # Delete command
      RM = rm -rf				
	  # Correct the path based on OS
      FixPath = $1				
	  # Name of the compiler used
	  CC = avr-gcc
	  # Name of the elf to hex file converter used
	  AVR_OBJ_CPY = avr-objcopy 
   endif
endif

# Command to make to consider these names as targets and not as file names in folder
.PHONY:all analysis clean doc

all:$(BUILD_DIR)
	# Compile the code and generate the ELF file
	$(CC) -g -Wall -Os -mmcu=atmega328 -DF_CPU=16000000UL $(INC) $(SRC) -o $(call FixPath,$(BUILD_DIR)/$(PROJ_NAME).elf)
	
hex: $(call FixPath,$(BUILD_DIR)/$(PROJ_NAME).elf)
	#create hex file
	$(OBJCOPY) $(HFLAGS) $< $(call FixPath,$(BUILD_DIR)/$(PROJ_NAME).hex)

$(BUILD_DIR):
	# Create directory to store the built files
	mkdir $(BUILD_DIR)
build_test : 
	gcc $(SRC) -o $(call FixPath,$(PROJ_NAME).$(EXEC)) -lm

run_test : build_test
	./$(call FixPath,$(PROJ_NAME).$(EXEC))
	
static_analysis:
	cppcheck --enable=all $(SRC)

clear :
	rm -r *.o *.elf *.hex *.out