EXTRA_DIST = *.h po/*

if SystemIncl
noinst_LTLIBRARIES = daq_System.la
daq_System_la_CXXFLAGS = -DMOD_INCL -fpic
daq_System_la_LIBTOOLFLAGS = --tag=disable-shared
daq_System_la_LDFLAGS = -module
else
oscd_modul_LTLIBRARIES = daq_System.la
daq_System_la_CXXFLAGS =
daq_System_la_LIBTOOLFLAGS = --tag=disable-static
daq_System_la_LDFLAGS = -module -avoid-version $(top_builddir)/src/liboscada.la
endif

daq_System_la_LDFLAGS += $(LIB_SENSORS)
daq_System_la_SOURCES = os_contr.cpp da_cpu.cpp da_mem.cpp da_uptime.cpp da_hddtemp.cpp da_sensors.cpp da_smart.cpp da_hddstat.cpp \
    da_netstat.cpp da_ups.cpp da_fs.cpp da_qsensor.cpp

I18N_mod = $(oscd_modulpref)System
include ../../../../I18N.mk
