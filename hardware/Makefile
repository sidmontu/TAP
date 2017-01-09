CC		:= iverilog
ARGS		:=
INCLUDE_PATH	:= ./include/
LIB_PATH	:= ./lib/

OBJ		:= alu
OBJ		+= register_file

HEADERS		:= include/common.h
HEADERS		+= include/alu.h

ALU_SRCS	:= src/alu.v

all: dir alu register_file

dir:
	mkdir -p bin;

alu: $(HEADERS) $(ALU_SRCS)
	@echo -n "Compiling ALU..."
	@$(CC) -obin/$@ -y$(LIB_PATH) -I$(INCLUDE_PATH) $(HEADERS) $(ALU_SRCS)
	@echo "Done."

register_file: $(HEADERS)
	@echo "Under construction.."

clean:
	rm -rf bin;
