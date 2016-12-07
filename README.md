# docker-TB-data
World Health Organization (WHO) on Tuberculosis data is used. It is stored in a CSV file that can be accessed via this page. Specifically, the TB burden estimates data is used. This data can be found <a href="https://extranet.who.int/tme/generateCSV.asp?ds=estimates">here</a>.

My Docker Hub repository can be found here:

https://hub.docker.com/r/jpatel7/tb-wf/

This repository contains two docker images, with tags: <b>nigeria</b> and <b>parameterized</b>

First image will calculate the average of number of Tuberculosis cases per 100000 people in Nigeria.
While running second image, we can calculate the average for any country dynamically by specifying country name in <i>docker run</i> command.
This average is calculated in a workflow using <a href="https://www.vistrails.org/index.php/Downloads"><b>VisTrails</b></a>.

You can pull these docker image using command:

<pre>docker pull jpatel7/tb-wf:nigeria</pre>
and
<pre>docker pull jpatel7/tb-wf:parameterized</pre>

You can run these images with following commands accordingly:
<pre>docker run jaypatel/tb-wf:nigeria</pre>
and
<pre>docker run jaypatel/tb-wf:parameterized country=Albania</pre>

Dockerfiles for both images and all other required files are uploaded in the repository.
