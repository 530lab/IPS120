# TODO

1) sometimes responds from the IPS120 mixes assignments of the magnetic field ans status values with eachothers: like output_field = self.ips120.query_status() or status = self.ips120.get_output_field(). Especially this happens when the regime is changed from clamped to hold right after the ips120 power supply is switched on and the program is used.

SOLVED! 

By adding a WHILE loop to methods where the values of magnetic field and status were being queried. This WHILE loop is checking the length of the response from the IPS120 and the match of it to the certain pattern.

2) Add a traceback and a possibility to record a log file. Because even there was no errors during the run
of the application, there was an error after the exact moment when the program was turned off by closing it.
This error can be connected with troubles of finishing the thread.

3) Add ZMQ
