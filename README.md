# proxmark3-vagrant-ubuntu
quick way for me to get proxmark3 dev up and running

You will probably need to manually configure USB on the VM machine settings
to attach the proxmark after VM is running

Mostly based on instructions from here
https://github.com/Proxmark/proxmark3/wiki/Ubuntu-Linux

The proxmark uses /dev/ttyACM0, which is dependent on the cdc_acm kernel module.

If you upgrade the kernel and /dev/ttyACM0 no longer shows up, make sure to install
- linux-image-extra-$(uname -r) for the current running kernel so that the cdc_acm kernel module is available
- sudo apt-get install linux-image-extra-$(uname -r)
