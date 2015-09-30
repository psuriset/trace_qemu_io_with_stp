# trace_qemu_io_with_stp

Trace reads/writes using systemtap

qemu-kvm binary has static probes and the RPM ships with a 
tapset with all the supported probes.  tapsets are in 
/usr/share/systemtap/tapset/qemu-kvm.stp

To write customized further check qemu code to find probes
which needs to be used and their values in trace-events

How to run

Start  IO workloads on VM and start tracing reads/writes of qemu. 
   
   for writes:

   stap bdrv_aio_writev.stp

   for reads:

   stap bdrv_aio_readv.stp


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/psuriset/trace_qemu_io_with_stp/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

