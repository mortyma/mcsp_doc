RSYNC = rsync
SSH = ssh

RFLAGS = --recursive --progress --copy-links --exclude=build/ --exclude=.git/ -e "$(SSH) -a"
SATURN = saturn
MARS = mars
REMOTEDIR = ~/mcsp_doc/benchmarks/
DEST = ./benchmarks/
SOURCE = ./graphs/


.PHONY: all protocol

all: to_mars from_mars
	
#saturn:
#	$(RSYNC) $(RFLAGS) $(SATURN):$(REMOTEDIR) $(DEST) 
	
to_mars:
	$(RSYNC) $(RFLAGS) ./graphs/ $(MARS):~/mcsp_doc/graphs/


from_mars:
	$(RSYNC) $(RFLAGS) $(MARS):~/mcsp_doc/benchmarks/mars/ ./benchmarks/mars/

protocol:
	$(MAKE) clean -C ./protocol/
	$(MAKE) -C ./protocol/
	
	