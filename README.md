# cs524-lab-2-solved
**TO GET THIS SOLUTION VISIT:** [CS524 Lab 2 Solved](https://www.ankitcodinghub.com/product/cs524-lab-2-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;91652&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS524 Lab 2 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
&nbsp;

In this assignment, you will learn to develop and load-balance your own infrastructure (a server farm) while applying your knowledge of DNS and other application entities and protocols.

You will also learn to use Cloud Storage for back-up and recovery of your data.

In addition, you will perform rudimentary analysis of the IP traffic.

You will use Nginx (a popular http server available at http://nginx.org/) to host a simple website on four Amazon EC2 instances; you will also configure an Nginx server on another instance, which will act as a load balancer. You will learn how to distribute networking workload across multiple servers.

A total of 100 points will be given to you if you successfully implement the outlined steps. In addition, at the discretion of course assistant, you can be given extra points (up to the maximum of 50) for devising and programming extra features.

As before, remember to double check the Amazon SLAs and ensure that you take all the necessary steps not to exceed the resource.

Please take the following steps:

1) Create the Amazon EC2 instances

You need to create five EC2 instances of the same type you have created in the previous Lab. One of these instances will act as a load balancer; the other four will act as web servers named Server1, Server2, Server3, Server4, as demonstrated below:

</div>
</div>
<div class="layoutArea">
<div class="column">
Incoming traffic |

Load Balancer

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
| ____________________________________ ||||

Server1 Server2 Server3 Server4

2) Install Nginx on each instance

After launching the instances, use amazon-linux-extras (the Amazon Linux native software manager) to

install Nginx on every instance and start the Nginx service.

To verify the Nginx is working, visit the hosted default webpage through instance’s public DNS from an

internet browser. You will see the Welcome message (if Nginx http server works properly).

You need to edit the default index.html file on four servers. This file can be found in the directory

/usr/share/nginx/html.

Use a text editor (such as vi) to Add the header with server ID in the index.html file like following: &lt;h1&gt;[SERVER_ID]&lt;/h1&gt;

Of course, you need to change SERVER_ID to the particular server name (i.e., Server1, Server2, Server3, or Server4).

3) Configure the load balancer

To configure the load balancer, you need to edit the load balancer’s configuration file

/etc/nginx/nginx.conf.

Use a text editor (such as vi) to replace the existing text with the following: events {

worker_connections 768; }

http {

upstream myapp {

#ip_hash;

server [SERVER_PUBLIC_DNS_NAME] weight=1;

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
server [SERVER_PUBLIC_DNS_NAME] weight=1; server [SERVER_PUBLIC_DNS_NAME] weight=1; server [SERVER_PUBLIC_DNS_NAME] weight=1; }

server {

listen 80;

server_name myapp.com; location / {

proxy_pass http://myapp;

} }

Again, you need to find the public DNS name of your servers and replace each occurrence of the SERVER_PUBLIC_DNS_NAME with the respective string.

The assignment server[&lt;name&gt;] weight=&lt;number&gt; establishes the weight of the server in the upstream cluster to be equal to the specified &lt;number&gt;. The present default is 1. To experiment with assigning some servers a greater proportion of the traffic, set weights correspondingly.

Restart the nginx service

You also need to replace the SERVER_PUBLIC_DNS part with the public DNS of your instances.

Now you can use the curl command in the shell to visit the balancer, which will distribute traffic among the servers.

$ curl [LOAD_BALANCER_DNS_NAME]

4) Collect the information on visits to your site

You can use the visit server tool, provided in the Appendix, or write your own tool, to track the distribution of the load. The tool visits the cluster 2000 times and returns the visit count on each server.

The following example illustrates the use of this tool:

$ visit_server.rb -d LOAD_BALANCER_DNS_NAME

The output would look like this:

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
Starting to visit load balancing server ————————-

Summary ————————- Server1 visit counts : 500 Server2 visit counts : 500 Server3 visit counts : 500 Server4 visit counts : 500 Total visit counts : 2000

The following table shows three different scenarios of weight combination of the four servers. Configure the nginx.conf file according to these scenarios. Then use visit_server for each scenario and record the outputs.

11111 21234 31212

Submission

Your submission should include a report that includes

1) the description of the steps that you have done in this assignment.

2) the results of the execution of the three scenarios 3) all additional observations.

</div>
</div>
<table>
<tbody>
<tr>
<td>
<div class="layoutArea">
<div class="column">
Server S cenario

</div>
</div>
<div class="layoutArea">
<div class="column">
Weight

</div>
</div>
</td>
<td>
<div class="layoutArea">
<div class="column">
Server 1

</div>
</div>
</td>
<td>
<div class="layoutArea">
<div class="column">
Server 2

</div>
</div>
</td>
<td>
<div class="layoutArea">
<div class="column">
Server 3

</div>
</div>
</td>
<td>
<div class="layoutArea">
<div class="column">
Server 4

</div>
</div>
</td>
</tr>
</tbody>
</table>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
Appendix: The Visit Server program #!/usr/bin/env ruby

#

<ul>
<li># &nbsp;This program is used for collecting web server visit information. #</li>
<li># &nbsp;Author: A. Genius #

require ‘optparse’ def print_usageputs “USAGE: visit_server -d DNS_NAME”

exit

end

# add option switch and handler

options = {}

option_parser = OptionParser.new do |opts|

# DNS_NAME argument

options[:dns_name] = nil

opts.on(‘-d’, ‘–dns-name DNS_NAME’, ‘Specify a DNS NAME’) { |dns_name|

options[:dns_name] = dns_name } # HELP argument

options[:help] = nil

opts.on(‘-h’, ‘–help’, ‘Display usage’) { |help| options[:help] = help } end
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
option_parser.parse!

# verify arguments

if options[:dns_name] then

dns_name = options[:dns_name] else

puts “Please set a balancer’s DNS.” print_usage

exit

end

if options[:help] then

print_usage

exit

end

# Keep STDOUT

#orig_stdout = $stdout

# redirect stdout to /dev/null

#$stdout = File.new(‘/dev/null’, ‘w’) server1_visit_count = 0

server2_visit_count = 0

server3_visit_count = 0

server4_visit_count = 0

# starting to visit load balancing server

puts “Starting to visit load balancing server” 2000.times do

</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="layoutArea">
<div class="column">
# visit load balancer

#o = `curl #{dns_name}`

o = `curl -s #{dns_name}`

if o =~ /server\s*1/i

server1_visit_count += 1

elsif o =~ /server\s*2/i

server2_visit_count += 1

elsif o =~ /server\s*3/i

server3_visit_count += 1

elsif o =~ /server\s*4/i

server4_visit_count += 1

end

print “.”

end

# redirect output to stdout

#$stdout = orig_stdout

# print visit information

puts

puts ‘————————-‘

puts ‘ Summary’

puts ‘————————-‘

puts “Server1 visit counts : ” + server1_visit_count.to_s puts “Server2 visit counts : ” + server2_visit_count.to_s puts “Server3 visit counts : ” + server3_visit_count.to_s

</div>
</div>
</div>
<div class="page" title="Page 8">
<div class="layoutArea">
<div class="column">
puts “Server4 visit counts : ” + server4_visit_count.to_s

puts “Total visit counts : ” + (server1_visit_count + server2_visit_count + server3_visit_count + server4_visit_count).to_s

Additional steps are outlined below.

Create EC2 by using command line

<ol>
<li>Use the `script` command to record all the commands you use to create the instance</li>
<li>Explain every step you have used to achieve your goal</li>
</ol>
After having deployed the balancer

<ol>
<li>Use the `tcpdump` command to collect all the packets that had been exchanged.</li>
<li>Analyze the packets and report your observations.</li>
</ol>
As an additional step, perform the EC2 backup and restore:

<ol>
<li>Register an AMI with your Load Balancer instance image and launch a new EC2 instance with that.</li>
<li>Verify that the new instance has all the files created in the load balancer instance. List and explain all the steps in achieving this goal.</li>
</ol>
Please provide screenshots to document your report.

</div>
</div>
</div>
