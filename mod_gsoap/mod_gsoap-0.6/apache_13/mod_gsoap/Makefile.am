#input for automake to generate mod_gsoap Makefile

AM_CPPFLAGS= $(CXXDEBUGDEFINES)
INCLUDES=-I$(top_builddir)

noinst_SCRIPTS=mod_gsoap.so

.c.so:
	apxs $(APXS_CXX_OPTIONS) -lgsoap++ $(INCLUDES) -c $< 
	#cp $@ `apxs -q LIBEXECDIR`

mod_gsoap.so : mod_gsoap.c

CLEANFILES=*~ *.o *.so


