BINARY=bin/tlogd
TARGET= $(BINARY)
HOME=../
CINC=-Iinclude -Itdr -I$(HOME)/tlibc/include -I$(HOME)/tlibc/tdr -I$(HOME)/tlog/include -I$(HOME)/tlog/tdr/ -I$(HOME)/tbusapi/include/ -I$(HOME)/tbus/include/ -I$(HOME)/tapp/include/
LDPATH=
DEPLIBS=-lpthread
TDRINC=-I$(HOME)/tlibc/tdr/ -I$(HOME)/tlog/tdr/
DEPOFILE=$(HOME)/tapp/lib/libtapp.a $(HOME)/tlog/lib/libtlog.a  $(HOME)/tbusapi/lib/libtbusapi.a $(HOME)/tbus/lib/libtbus.a $(HOME)/tlibc/lib/libtlibc.a
CFILE=$(wildcard source/*.c)
TYPES_TDR_FILE=$(wildcard tdr/*.tdr)
READER_TDR_FILE=$(wildcard tdr/*.tdr)

include $(HOME)/build.mk

dep:
	@mkdir -p bin

install:
	mkdir -p $(PREFIX)
	cp -rf bin $(PREFIX)
	cp -rf tdr $(PREFIX)
	find $(PREFIX) -name "*.d" -or -name "*.o" | xargs rm -f
