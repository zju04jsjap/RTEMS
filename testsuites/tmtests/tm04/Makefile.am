
rtems_tests_PROGRAMS = tm04
tm04_SOURCES = task1.c system.h ../include/timesys.h \
    ../../support/src/tmtests_empty_function.c

dist_rtems_tests_DATA = tm04.doc

include $(RTEMS_ROOT)/make/custom/@RTEMS_BSP@.cfg
include $(top_srcdir)/../automake/compile.am
include $(top_srcdir)/../automake/leaf.am


OPERATION_COUNT = @OPERATION_COUNT@
AM_CPPFLAGS += -I$(top_srcdir)/include -DOPERATION_COUNT=$(OPERATION_COUNT)
AM_CPPFLAGS += -I$(top_srcdir)/../support/include

LINK_OBJS = $(tm04_OBJECTS)
LINK_LIBS = $(tm04_LDLIBS)

tm04$(EXEEXT): $(tm04_OBJECTS) $(tm04_DEPENDENCIES)
	@rm -f tm04$(EXEEXT)
	$(make-exe)

include $(top_srcdir)/../automake/local.am
