!renesas rzg2l manifest VLP 4.00!

repo init -u https://github.com/perplerain/VLP4 -m manifest-renesas.xml

repo sync

Need to download codec & graphics-lib

https://www.renesas.com/en/document/swo/rz-mpu-graphics-library-v4125-rzg2l-and-rzg2lc-rtk0ef0045z14001zj-v4125enzip?r=25573698

https://www.renesas.com/en/document/swo/rz-mpu-video-codec-library-evaluation-version-v4130-rzg2l-rtk0ef0045z16001zjv4130enzip?r=25573698

After downloading the proprietary package, please decompress them then put meta-rz-features folder at $WORK folder.

############## Build ###########

TEMPLATECONF=$PWD/meta-renesas/meta-rzg2l/docs/template/conf/ source poky/oe-init-build-env build
