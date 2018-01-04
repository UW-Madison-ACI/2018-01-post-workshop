---
layout: workshop      # DON'T CHANGE THIS.
carpentry: "swc"    # what kind of Carpentry (must be either "lc" or "dc" or "swc")
venue: "Post-Carpentry Sessions @ UW Madison"        # brief name of host site without address (e.g., "Euphoric State University")
address: "Discovery Building, Room 1170"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "us"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1)
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/ISO_639-1)
latlng: "43.072912,-89.408079"       # decimal latitude and longitude of workshop venue (e.g., "41.7901128,-87.6007318" - use http://www.latlong.net/)
humandate: "January 16-19, 2018"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "10am - noon"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2018-01-16      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2018-01-19        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["see below"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
#helper: [" "]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["ckoch5@wisc.edu"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:             # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

{% comment %} See instructions in the comments below for 
how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
  HEADER

  Edit the values in the block above to be appropriate for your workshop.
  If the value is not 'true', 'false', 'null', or a number, please use
  double quotation marks around the value, unless specified otherwise.
  And run 'bin/workshop_check.py' *before* committing to make sure that changes are good.
{% endcomment %}

{% comment %}
  EVENTBRITE

  This block includes the Eventbrite registration widget if
  'eventbrite' has been set in the header.  You can delete it if you
  are not using Eventbrite, or leave it in, since it will not be
  displayed if the 'eventbrite' field in the header is not set.
{% endcomment %}
{% if page.eventbrite %}
<iframe
  src="https://www.eventbrite.com/tickets-external?eid={{page.eventbrite}}&ref=etckt"
  frameborder="0"
  width="100%"
  height="248px"
  scrolling="auto">
</iframe>
{% endif %}

<h2 id="general">General Information</h2>

<p>Do you still have questions or want to learn more about the topics we 
covered in Software and Data Carpentry?  We are offering four follow-up sessions 
hosted by our Software and Data Carpentry instructors, in order to review material 
from the workshops, demonstrate additional features, and provide a place for 
questions and consultation.  We will NOT be providing a basic introduction to 
any topics -- these sessions assume that you have at least seen and tried using 
the relevant tool, based on attending a Software or Data Carpentry workshop.  </p>

<p>We will offer the following topics on the following days:</p>

<hr>

 <div class="row">
    <div class="col-md-3">
    <h3>Shell</h3>
    <p>Tuesday, January 16</p>
    <p>10am - noon</p>
    <p><a href="#shell">more details</a></p>
    </div>
    <div class="col-md-3">
    <h3>Git</h3>
    <p>Wednesday, January 17</p>
    <p>10am - noon</p>
    <p><a href="#git">more details</a></p>
    </div>
    <div class="col-md-3">
    <h3>R</h3>
    <p>Thursday, January 18</p>
    <p>10am - noon</p>
    <p><a href="#r">more details</a></p>
    </div>
    <div class="col-md-3">
    <h3>Python</h3>
    <p>Friday, January 19</p>    
    <p>10am - noon</p>
    <p><a href="#python">more details</a></p>
    </div>
 </div>
 
<hr>

<p>Please see the descriptions below for more information and how to sign up. We 
reserve the right to cancel a session due to projected low attendance (fewer than 4-5 
people) so please register if you're planning to come!</p>
 
{% comment %}
  AUDIENCE

  Explain who your audience is.  (In particular, tell readers if the
  workshop is only open to people from a particular institution.
{% endcomment %}

<p id="who">
  <strong>Who:</strong>
  These sessions are for graduate students and other researchers who have 
  previously attended any Software or Data Carpentry workshop.
</p>

{% comment %}
  SPECIAL REQUIREMENTS

  Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
  <strong>Requirements:</strong> Bring a laptop to use.  Based on previous 
  participation in workshops, the appropriate software or tools should be 
  already installed.  
</p>

{% comment %}
  LOCATION

  This block displays the address and links to maps showing directions
  if the latitude and longitude of the workshop have been set.  You
  can use http://itouchmap.com/latlong.html to find the lat/long of an
  address.
{% endcomment %}
{% if page.latlng %}
<p id="where">
  <strong>Where:</strong>
  {{page.address}}.
  Get directions with
  <a href="//www.openstreetmap.org/?mlat={{page.latlng | replace:',','&mlon='}}&zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q={{page.latlng}}">Google Maps</a>.
</p>
{% endif %}

{% comment %}
  ACCESSIBILITY

  Modify the block below if there are any barriers to accessibility or
  special instructions.
{% endcomment %}
<p id="accessibility">
  <strong>Accessibility:</strong> The workshop organisers have checked that:
</p>
<ul>
  <li>The room is wheelchair / scooter accessible.</li>
  <li>Accessible restrooms are available.</li>
</ul>

{% comment %}
  CONTACT EMAIL ADDRESS

  Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
  Please email
  {% if page.email %}
    {% for email in page.email %}
      {% if forloop.last and page.email.size > 1 %}
        or
      {% else %}
        {% unless forloop.first %}
        ,
        {% endunless %}
      {% endif %}
      <a href='mailto:{{email}}'>{{email}}</a>
    {% endfor %}
  {% else %}
    to-be-announced
  {% endif %}
  for more information.
</p>

<hr/>

{% comment %}
  SCHEDULE

  Show the workshop's schedule.  Edit the items and times in the table
  to match your plans.  You may also want to change 'Day 1' and 'Day
  2' to be actual dates or days of the week.
{% endcomment %}
<h2 id="schedule">Sessions</h2>

<a name="shell"></a>
<div class="jumbotron">
<h3>Shell</h3>
<p><strong>Date/Time:</strong> Tuesday, January 16, 2018; 10am - noon</p>
<p><strong>Facilitators:</strong> Carolyn Voter, Paul Wilson</p>
<p><strong>Topics covered:</strong> </p>
<p><a href="https://www.eventbrite.com/e/workshop-follow-up-shell-tickets-41794385131">Sign Up Here</a></p>
</div>

<a name="git"></a>
<div class="jumbotron">
<h3>Git</h3>
<p><strong>Date/Time:</strong> Wednesday, January 17, 2018; 10am - noon</p>
<p><strong>Facilitators:</strong> Patrick Shriwise, Steve Goldstein</p>
<p><strong>Topics covered:</strong> </p>
<p><a href=" ">Sign Up Here</a></p>
</div>

<a name="r"></a>
<div class="jumbotron">
<h3>R</h3>
<p><strong>Date/Time:</strong> Thursday, January 18, 2018; 10am - noon</p>
<p><strong>Facilitators:</strong> Brian Yandell, Alex Bajcz, Richard Barker</p>
<p><strong>Topics covered:</strong> </p>
<p><a href=" ">Sign Up Here</a></p>
</div>

<a name="python"></a>
<div class="jumbotron">
<h3>Python</h3>
<p><strong>Date/Time:</strong> Friday, January 19, 2018; 10am - noon</p>
<p><strong>Facilitators:</strong> Sarah Stevens, Taylor Scott</p>
<p><strong>Topics covered:</strong> </p>
<p><a href=" ">Sign Up Here</a></p>
</div>