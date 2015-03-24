# Laser Locator

This version of AprilCal has been modified to extract the luma channel of whatever source it's receiving and transmit it via TCP port 7001 (localhost).

The objective is to enable AprilCal to work with the MPEG4/H.264 IP cameras supported by the FFMPEG package.

To use with AprilCal, run AprilCal in one window:
% java april.camera.calibrator.AprilCal -u tcp-server://7001

and the modified ffplay in another:

% ./ffplay -rtsp_transport tcp rtsp://192.168.1.44/

