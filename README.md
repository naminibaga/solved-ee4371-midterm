Download Link: https://assignmentchef.com/product/solved-ee4371-midterm
<br>
A mix of video on demand and data packets arrive at a router along a high bandwidth link. The router has to schedule them to a home client through a low bandwidth link (512 kbps or 64 kbytes per second). The data packets are somewhat sensitive to delay (not more than 30 seconds delay permitted) while the video on demand is very delay sensitive (max of 1 second delay is acceptable) and arrive at a rate of 48 kbytes per second. The data packets are 1024 bytes in size, while the video packets are 512 bytes long. You are to keep dropped video packet rates to below 5% every second (your algorithm should take this into account), and can drop data packets but should minimize the number dropped. Dropped packets are retransmitted, which increases the bandwidth required at a later time.

For the problem on hand, the queue is empty and <u>a 512 kbyte burst of data packets arrives at <em>t </em></u><u>=0 and has to be scheduled</u>. Further data packets arrive at the middle of each second, of size 6 kBytes (plus retransmitted packets dropped previous second). Video packets arrive at fixed intervals starting at <em>t </em>=0<sup>+ </sup>(just after the arrival of data packets).

<h1>Video</h1>

The figure above shows when data and video packets arrive. The queue size is very large and it does not overflow.

<ol>

 <li>Suppose we only have the video packets and the periodic data pack- . . . . . . . . . . . . . . . . . [10] ets, but no initial burst of data packets. Design a FIFO queue into which all the packets are inserted as they arrive. Give pseudocode for the queue. There is a period of waiting, and a period of transmission. Include both to compute the delay for each type packet. Assuming packets come out in the order they arrive, what % of dropped packets of each type (data or video) will there be over the first 30 seconds? Does this meet requirements?</li>

</ol>

1

<ol start="2">

 <li>Suppose the burst of data packets at <em>t </em>=0 also happened. How does . . . . . . . . . . . . . . . . . [10] your answer change if you consider the first 30 seconds? How does retransmission of dropped data packets affect your answer?</li>

 <li>Suppose at entry, video packets are always inserted at “front” of . . . . . . . . . . . . . . . . . [10] the queue, while the data packets are inserted at the “end” (queue length is unlimited, which means here “very large”). The order of packets in the queue should be preserved for video packets (i.e., first one received should be the first one dequeued. Give pseudocode for this and discuss if it will work. Which type of queue is best? What is the value function that ensures video packets are queued in front? What % of dropped packets of each type will there be over the next 30 seconds?</li>

 <li>Create the program that implements Q2 and Q3. The program . . . . . . . . . . . . . . . . . [20] should create output to show the status at the end of each second as follows:</li>

</ol>

<table width="527">

 <tbody>

  <tr>

   <td width="48">Time</td>

   <td width="75">Q Length</td>

   <td width="48">Time</td>

   <td width="58">Condn</td>

   <td width="56">HTTP</td>

   <td width="52">Video</td>

   <td width="97">HTTP Drops</td>

   <td width="93">Video Drops</td>

  </tr>

  <tr>

   <td width="48">0</td>

   <td width="75">512</td>

   <td width="48">0</td>

   <td width="58">?</td>

   <td width="56">?</td>

   <td width="52">?</td>

   <td width="97">?</td>

   <td width="93">?</td>

  </tr>

 </tbody>

</table>

where “Condn” is the condition you used to decide whether to drop video packets, HTTP is the number of kBytes of HTTP sent this second, and Video is the number of kBytes of Video sent this second.