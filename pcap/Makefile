include $(GOROOT)/src/Make.inc

TARG=gopcap.googlecode.com/hg/pcap
GOFILES=decode.go
CGOFILES=pcap.go
CGO_LDFLAGS=-lpcap
CLEANFILES=pcaptest tcpdump

include $(GOROOT)/src/Make.pkg

pcaptest: pcaptest.go install
	$(GC) pcaptest.go
	$(LD) -o $@ pcaptest.$(O)

tcpdump: tcpdump.go install
	$(GC) tcpdump.go
	$(LD) -o $@ tcpdump.$(O)
