# contrib/btree_gist/Makefile

MODULE_big  = btree_gist

OBJS        = btree_gist.o btree_utils_num.o btree_utils_var.o btree_int2.o btree_int4.o btree_int8.o \
              btree_float4.o btree_float8.o btree_cash.o btree_oid.o btree_ts.o btree_time.o \
              btree_date.o btree_interval.o btree_macaddr.o btree_inet.o btree_text.o \
              btree_bytea.o btree_bit.o btree_numeric.o

DATA_built  = btree_gist.sql
DATA        = uninstall_btree_gist.sql

REGRESS     = init int2 int4 int8 float4 float8 cash oid timestamp timestamptz time timetz \
              date interval macaddr inet cidr text varchar char bytea bit varbit numeric not_equal

ifdef USE_PGXS
PG_CONFIG = pg_config
PGXS := $(shell $(PG_CONFIG) --pgxs)
include $(PGXS)
else
subdir = contrib/btree_gist
top_builddir = ../..
include $(top_builddir)/src/Makefile.global
include $(top_srcdir)/contrib/contrib-global.mk
endif
