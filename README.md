# camcam

CamCam is HowTo how to use RaspBerry computer with WebCam.

# Preparing awesome MotionPlus project for manage your WebCam

    Tested by me with a RaspBerry Pi4B - PI OS - Debian BullsEye 32bit arm.
    Tested by me with noname WebCam attached to the USB2.0 port.

Install basic build packages:
    sudo apt install autoconf automake autopoint build-essential pkgconf libtool libzip-dev
          libjpeg-dev git libavformat-dev libavcodec-dev libavutil-dev libswscale-dev libavdevice-dev
          libwebp-dev gettext libmicrohttpd-dev libmariadb-dev libasound2-dev libfftw3-dev

Clone repository:
    git clone --recursive https://github.com/Motion-Project/motionplus.git

Once required packages are installed, execute:
    autoreconf -fiv
    ./configure
    make
    make install

Sample custom configuration options:
    --prefix               :  Specify the install location for the motion package
    --with-ffmpeg=[dir]    :  Specify the location in which ffmpeg/libav is installed.

Configure - or use included in this repo
    /usr/local/etc/motionplus/motionplus-dist.conf
and
    /use/local/etc/motionplus/camera1-dist.conf

run
    sudo motionplus -c /usr/local/etc/motionplus/motionplus-dist.conf

web access
    open url in your web browser "192.168.x.y:8085"

enjoy :-)




