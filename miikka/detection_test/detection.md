We became suspicious if the training had any effect at all, so we decided to stage a very small scale test.

I took around 20 pictures of two empty bottles and a computer mouse, and went through the process of preparing them for training. 

Then I commenced training as per usual:

	./darknet detector train obj.data yolov3-tiny.cfg darknet19_448.conv.23

After around 30 000 iterations, I stopped the training.

I then took some video of bottles and the computer mouse used, and tested if they would be detected now:

	./darknet detector test obj.data yolov3-tiny.cfg yolov3-tiny_30000.weights

<video width="320" height="240">
  <source src="Results.gif" type="video/gif">
</video>

It's not much but it IS something! The object name is totally wrong, but at least now we can be sure that our training actually does SOMETHING. Now it's just a matter of making it do the right things.
