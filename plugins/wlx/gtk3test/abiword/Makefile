CC = gcc
CFLAGS =
INCLUDES = `pkg-config --cflags --libs abiword-3.0`
PLGNAME = abiword_tst.wlx
PLGFLAGS = -shared -fPIC -Wl,--no-as-needed
PLGINCLUDES = `pkg-config --cflags --libs gtk+-2.0` -I../../../sdk


all:   plugin crapkostyl

crapkostyl:
		$(CC) $(CFLAGS) $(INCLUDES) kostyl.c -o kostyl

plugin:
		$(CC) $(PLGFLAGS) $(PLGINCLUDES) plugin.c -o $(PLGNAME)

clean:
		$(RM) $(PLGNAME) kostyl
