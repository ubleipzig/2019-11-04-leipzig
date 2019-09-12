---
layout: workshop      # DON'T CHANGE THIS.
carpentry: "lc"    # what kind of Carpentry (must be either "lc" or "dc" or "swc").  
                      # Be sure to update the Carpentry type in _config.yml as well.  
venue: "Library Carpentry, Universitätsbibliothek Leipzig"        # brief name of host site without address (e.g., "Euphoric State University")
address: "Schulungsraum (1. OG) der Bibliothek Medizin/Naturwissenschaften, Liebigstraße 23/25, 04103 Leipzig"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "de"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes)
language: "de"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)
latlng: "51.33155, 12.38978"       # decimal latitude and longitude of workshop venue (e.g., "41.7901128,-87.6007318" - use https://www.latlong.net/)
humandate: "04. - 05. November 2019"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "09:00 - 16:30"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2019-11-04      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2019-11-05        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Martin Czygan", "Ronny Gey", "Tracy Hoffmann", "Peter Mühleder", "Florian Rämisch"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: [""]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["gey@ub.uni-leipzig.de", "czygan@ub.uni-leipzig.de"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes: https://pad.carpentries.org/2019-11-04-leipzig     # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

{% comment %} See instructions in the comments below for how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
HEADER

Edit the values in the block above to be appropriate for your workshop.
If the value is not 'true', 'false', 'null', or a number, please use
double quotation marks around the value, unless specified otherwise.
And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}


{% if page.carpentry != site.carpentry %}
<div class="alert alert-warning">
You specified <code>carpentry: {{page.carpentry}}</code> in <code>index.md</code> and
<code>carpentry: {{site.carpentry}}</code> in <code>_config.yml</code>. Make sure you edit both files. After editing <code>_config.yml</code>, you need to run <code>make serve</code> again to 
see the changes take effect locally.
</div>
{% endif %}

<h2 id="general">Allgemeine Informationen</h2>

{% comment %}
INTRODUCTION

Edit the general explanatory paragraph below if you want to change
the pitch.
{% endcomment %}
{% if page.carpentry == "swc" %}
{% include sc/intro.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}

{% comment %}
AUDIENCE

Explain who your audience is.  (In particular, tell readers if the
workshop is only open to people from a particular institution.
{% endcomment %}
{% if page.carpentry == "swc" %}
{% include sc/who.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/who.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/who.html %}
{% endif %}

{% comment %}
LOCATION

This block displays the address and links to maps showing directions
if the latitude and longitude of the workshop have been set.  You
can use https://itouchmap.com/latlong.html to find the lat/long of an
address.
{% endcomment %}
{% if page.latlng %}
<p id="where">
  <strong>Wo:</strong>
  {{page.address}}.
  Wegbeschreibung mit
  <a href="//www.openstreetmap.org/?mlat={{page.latlng | replace:',','&mlon='}}&zoom=16">OpenStreetMap</a>
  oder
  <a href="//maps.google.com/maps?q={{page.latlng}}">Google Maps</a>.
</p>
{% endif %}

{% comment %}
DATE

This block displays the date and links to Google Calendar.
{% endcomment %}
{% if page.humandate %}
<p id="when">
  <strong>Wann:</strong>
  {{page.humandate}}.
  {% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
SPECIAL REQUIREMENTS

Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
  <strong>Anforderungen:</strong> Die Teilnehmer müssen einen Laptop mit einem Mac-, Linux- oder Windows-Betriebssystem (kein Tablett, Chromebook usw.) mitbringen, auf dem sie über Administratorrechte verfügen. Sie sollten ein paar spezifische Softwarepakete installiert haben (aufgeführt <a href="#setup">hier</a>).
</p>

{% comment%}
CODE OF CONDUCT
{% endcomment %}
<p id="code-of-conduct">
<strong>Verhaltenskodex:</strong> Jeder, der an einer Carpentries-Veranstaltung teilnimmt, ist verpflichtet, sich an den  <a href="https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html">Verhaltenskodex</a> zu halten. Dieses Dokument beschreibt auch, wie man bei Bedarf einen Vorfall melden kann.
</p>


{% comment %}
ACCESSIBILITY

Modify the block below if there are any barriers to accessibility or
special instructions.
{% endcomment %}
<p id="accessibility">
  <strong>Zugang:</strong> Wir sind bestrebt, diesen Workshop für alle zugänglich zu machen. Die Organisatoren des Workshops haben überprüft, dass:
</p>
<ul>
  <li>der Schulungsraum rollstuhlgerecht ist.</li>
  <li>zugängliche Toiletten vorhanden sind.</li>
</ul>
<p>
  Die Materialien werden vor dem Workshop zur Verfügung gestellt und bei Bedarf können großformatige Handzettel gereicht werden, was den Organisatoren vorab mitgeteilt werden sollte. Um Ihnen das Lernen zu erleichtern (z.B. Gebärdensprachdolmetscher, Vorkehrungen für stillende Mütter), bitten wir Sie, uns vorab zu informieren. Nehmen Sie Kontakt auf (unter Verwendung der untenstehenden Kontaktdaten) und wir werden versuchen, Ihnen weiterzuhelfen.
</p>

<p id="contact">
  <strong>Zahlungsinformationen</strong>:
  folgen
</p>

<p id="contact">
  <strong>Registrierung</strong>:
  folgt
</p>

<p id="contact">
  <strong>Organisation</strong>:
Wir freuen uns über die finanzielle Unterstützung dieses Workshops durch den VDB (Verein Deutscher Bibliothekarinnen und Bibliothekare). Der Workshop wird gemeinsam vom Regionalverband Sachsen - Sachsen-Anhalt - Thüringen und der Universitätsbibliothek Leipzig organisiert.
</p>

{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Kontakt</strong>:
  Sie erreichen uns unter 
  {% if page.email %}
  {% for email in page.email %}
  {% if forloop.last and page.email.size > 1 %}
  oder
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
  für weitere Informationen.
</p>

<hr/>
<p>
<a href="https://www.vdb-online.org"> 
   <img src="assets/img/VDB_Logo_RGB_400px.jpg" alt="VDB" height="100"/>
 </a>
 <a href="https://www.ub.uni-leipzig.de">
   <img src="assets/img/UBL_Logo_Blau.png" alt="UB Leipzig" height="100" align="right"/>
 </a>
</p>
<hr/>

{% comment %} 
SURVEYS - DO NOT EDIT SURVEY LINKS 
{% endcomment %}
<h2 id="surveys">Umfragen</h2>
<p>Bitte stellen Sie sicher, dass Sie diese Umfragen vor und nach dem Workshop ausfüllen (Umfragen auf Englisch).</p>
{% if site.carpentry == "swc" %} 
<p><a href="{{ site.swc_pre_survey }}{{ site.github.project_title }}">Umfrage vor dem Workshop</a></p>
<p><a href="{{ site.swc_post_survey }}{{ site.github.project_title }}">Umfrage nach dem Workshop</a></p>
{% elsif site.carpentry == "dc" %}
<p><a href="{{ site.dc_pre_survey }}{{ site.github.project_title }}">Umfrage vor dem Workshop</a></p>
<p><a href="{{ site.dc_post_survey }}{{ site.github.project_title }}">Umfrage nach dem Workshop</a></p>
{% elsif site.carpentry == "lc" %}
<p><a href="{{ site.lc_pre_survey }}{{ site.github.project_title }}">Umfrage vor dem Workshop</a></p>
<p><a href="{{ site.lc_post_survey }}{{ site.github.project_title }}">Umfrage nach dem Workshop</a></p>
{% endif %}

<hr/>


{% comment %}
SCHEDULE

Show the workshop's schedule.  Edit the items and times in the table
to match your plans.  You may also want to change 'Day 1' and 'Day
2' to be actual dates or days of the week.
{% endcomment %}
<h2 id="schedule">Schedule</h2>

{% if page.carpentry == "swc" %}
{% include sc/schedule.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/schedule.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/schedule.html %}
{% endif %}

{% comment %}
Collaborative Notes

If you want to use an Etherpad, go to

http://pad.carpentries.org/YYYY-MM-DD-site

where 'YYYY-MM-DD-site' is the identifier for your workshop,
e.g., '2015-06-10-esu'.
{% endcomment %}
{% if page.collaborative_notes %}
<p id="collaborative_notes">
  Wir werden dieses <a href="{{page.collaborative_notes}}}">kollaborative Dokument</a> zum Chatten, Notieren und Teilen von URLs und Code verwenden.
</p>
{% endif %}

<hr/>

{% comment %}
SYLLABUS

Show what topics will be covered.

1. If your workshop is R rather than Python, remove the comment
around that section and put a comment around the Python section.
2. Some workshops will delete SQL.
3. Please make sure the list of topics is synchronized with what you
intend to teach.
4. You may need to move the div's with class="col-md-6" around inside
the div's with class="row" to balance the multi-column layout.

This is one of the places where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}
<h2 id="syllabus">Ablauf</h2>

{% if page.carpentry == "swc" %}
{% include sc/syllabus.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/syllabus.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/syllabus.html %}
{% endif %}

<hr/>

{% comment %}
SETUP

Delete irrelevant sections from the setup instructions.  Each
section is inside a 'div' without any classes to make the beginning
and end easier to find.

This is the other place where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}

<h2 id="setup">Setup</h2>

<p>
  Um an einem
  {% if page.carpentry == "swc" %}
  Software Carpentry
  {% elsif page.carpentry == "dc" %}
  Data Carpentry
  {% elsif page.carpentry == "lc" %}
  Library Carpentry
  {% endif %}
  Workshop teilzunehmen, benötigen Sie Zugriff auf die unten beschriebene Software. Außerdem benötigen Sie einen aktuellen Webbrowser. Die Installationsanleitungen sind momentan lediglich auf Englisch verfügbar.
</p>
<p>
  Wir führen eine Liste der häufigsten Probleme, die während der Installation auftreten können: 
  <a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Wiki-Seite Konfigurationsprobleme und Lösungen</a>.
</p>

<div id="shell"> {% comment %} Start of 'shell' section. {% endcomment %}
  <h3>Die Bash Shell</h3>
  <p>
    Bash ist eine häufig verwendete Shell, die Ihnen die Möglichkeit gibt, einfache Aufgaben schneller zu erledigen.
  </p>

  <div>
    <ul class="nav nav-tabs nav-justified" role="tablist">
      <li role="presentation" class="active"><a data-os="windows" href="#shell-windows" aria-controls="Windows" role="tab" data-toggle="tab">Windows</a></li>
      <li role="presentation"><a data-os="macos" href="#shell-macos" aria-controls="MacOS" role="tab" data-toggle="tab">MacOS</a></li>
      <li role="presentation"><a data-os="linux" href="#shell-linux" aria-controls="Linux" role="tab" data-toggle="tab">Linux</a></li>
    </ul>

    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="shell-windows">
        <a href="https://www.youtube.com/watch?v=339AEqk9c-8">Video Tutorial</a>
        <ol>
          <li>Download the Git for Windows <a href="https://git-for-windows.github.io/">installer</a>.</li>
          <li>Run the installer and follow the steps below:
            <ol>
              {% comment %} Git 2.22.0 Setup {% endcomment %}
              <li>
                Click on "Next" four times (two times if you've previously
                installed Git).  You don't need to change anything
                in the Information, location, components, and start menu screens.
              </li>
              <li>
                <strong>
                  Select "Use the nano editor by default" and click on "Next".
                </strong>
              </li>
              {% comment %} Adjusting your PATH environment {% endcomment %}
              <li>
                Keep "Git from the command line and also from 3rd-party software" selected and click on "Next".
                If you forgot to do this programs that you need for the workshop will not work properly.
                If this happens rerun the installer and select the appropriate option.
              </li>
              {% comment %} Choosing the SSH executable {% endcomment %}
              <li>Click on "Next".</li>
              {% comment %} Choosing HTTPS transport backend {% endcomment %}
              <li>Select "Use the native Windows Secure Channel library", and click "Next".</li>
              {% comment %} This should mean that people stuck behind corporate firewalls that do MITM attacks 
                                 with their own root CA are still able to access remote git repos. {% endcomment %}
              {% comment %} Configuring the line ending conversions {% endcomment %}
              <li>
                Keep "Checkout Windows-style, commit Unix-style line endings" selected and click on "Next".
              </li>
              {% comment %} Configuring the terminal emulator to use with Git Bash {% endcomment %}
              <li>
                <strong>
                  Select "Use Windows' default console window" and click on "Next".
                </strong>
              </li>
              {% comment %} Configuring extra options {% endcomment %}
              <li>Leave all three items selected, and click on "Next".</li>
              {% comment %} Configuring experimental options {% endcomment %}
              <li>Do not select the experimental option. Click "Install".</li>
              {% comment %} Installing {% endcomment %}
              {% comment %} Completing the Git Setup Wizard {% endcomment %}
              <li>Click on "Finish".</li>
            </ol>
          </li>
          <li>
            If your "HOME" environment variable is not set (or you don't know what this is):
            <ol>
              <li>Open command prompt (Open Start Menu then type <code>cmd</code> and press [Enter])</li>
              <li>
                Type the following line into the command prompt window exactly as shown:
                <p><code>setx HOME "%USERPROFILE%"</code></p>
              </li>
              <li>Press [Enter], you should see <code>SUCCESS: Specified value was saved.</code></li>
              <li>Quit command prompt by typing <code>exit</code> then pressing [Enter]</li>
            </ol>
          </li>
        </ol>
        <p>This will provide you with both Git and Bash in the Git Bash program.</p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="shell-macos">
        <p>
          The default shell in all versions of macOS is Bash, so no
          need to install anything.  You access Bash from the Terminal
          (found in
          <code>/Applications/Utilities</code>).
          See the Git installation <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">video tutorial</a>
          for an example on how to open the Terminal.
          You may want to keep
          Terminal in your dock for this workshop.
        </p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="shell-linux">
        <p>
          The default shell is usually Bash, but if your
          machine is set up differently you can run it by opening a
          terminal and typing <code>bash</code>.  There is no need to
          install anything.
        </p>
      </article>
    </div>
  </div>
</div> {% comment %} End of 'shell' section. {% endcomment %}

<div id="git"> {% comment %} Start of 'Git' section. GitHub browser compatibility
  is given at https://help.github.com/articles/supported-browsers/{% endcomment %}
  <h3>Git</h3>
  <p>
    Git ist ein Versionskontrollsystem, mit dem Sie verfolgen können, wer wann welche Änderungen vorgenommen hat. Es verfügt über Optionen, um freigegebene oder öffentliche Versionen Ihres Quellcodes auf <a href="https://github.com/">github.com</a> einfach zu aktualisieren. Sie benötigen einen <a href="https://help.github.com/articles/supported-browsers/">unterstützten Webbrowser</a>.
  </p>
  <p>Sie benötigen ein Konto unter <a href="https://github.com/">github.com</a> für Teile des Git-Workshops. GitHub-Basiskonten sind kostenlos. Wir empfehlen Ihnen, ein GitHub-Konto zu erstellen, wenn Sie noch kein Konto haben. Bitte überlegen Sie, welche persönlichen Daten Sie preisgeben möchten. Zum Beispiel können Sie Sich diese <a href="https://help.github.com/articles/keeping-your-email-address-private/">Anleitung ansehen, um Ihre E-Mail-Adresse privat zu halten</a>, die Sie bei GitHub nutzen.</p>

  <div>
    <ul class="nav nav-tabs nav-justified" role="tablist">
      <li role="presentation" class="active"><a data-os="windows" href="#git-windows" aria-controls="Windows" role="tab" data-toggle="tab">Windows</a></li>
      <li role="presentation"><a data-os="macos" href="#git-macos" aria-controls="MacOS" role="tab" data-toggle="tab">MacOS</a></li>
      <li role="presentation"><a data-os="linux" href="#git-linux" aria-controls="Linux" role="tab" data-toggle="tab">Linux</a></li>
    </ul>

    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="git-windows">
        <p>
          Git should be installed on your computer as part of your Bash
          install (described above).
        </p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="git-macos">
        <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">Video Tutorial</a>
        <p>
          <strong>For OS X 10.9 and higher</strong>, install Git for Mac
          by downloading and running the most recent "mavericks" installer from
          <a href="http://sourceforge.net/projects/git-osx-installer/files/">this list</a>.
          Because this installer is not signed by the developer, you may have to
          right click (control click) on the .pkg file, click Open, and click
          Open on the pop up window. 
          After installing Git, there will not be anything in your <code>/Applications</code> folder,
          as Git is a command line program.
          <strong>For older versions of OS X (10.5-10.8)</strong> use the
          most recent available installer labelled "snow-leopard"
          <a href="http://sourceforge.net/projects/git-osx-installer/files/">available here</a>.
        </p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="git-linux">
        <p>
          If Git is not already available on your machine you can try to
          install it via your distro's package manager. For Debian/Ubuntu run
          <code>sudo apt-get install git</code> and for Fedora run
          <code>sudo dnf install git</code>.
        </p>
      </article>
    </div>
  </div>
</div> {% comment %} End of 'Git' section. {% endcomment %}

<div id="editor"> {% comment %} Start of 'editor' section. {% endcomment %}
  <h3>Text Editor</h3>

  <p>
    Wenn Sie Code schreiben, ist es sehr nützlich, einen Texteditor zu haben, der für das Schreiben von Code optimiert ist, mit Funktionen wie der automatischen Farbcodierung von Schlüsselwörtern. Der Standard-Text-Editor unter MacOS und Linux ist normalerweise auf Vim eingestellt, der nicht gerade für seine intuitive Bedienung bekannt ist. Wenn Sie versehentlich darin stecken geblieben sind, drücken Sie die Taste <kbd>Esc</kbd>, gefolgt von <kbd>:</kbd>+<kbd>Q</kbd>+<kbd>!</kbd> (Doppelpunkt, Kleinbuchstabe 'q', Ausrufezeichen) und drücken Sie dann <kbd>Return</kbd>, um zur Shell zurückzukehren.
  </p>

  <div>
    <ul class="nav nav-tabs nav-justified" role="tablist">
      <li role="presentation" class="active"><a data-os="windows" href="#editor-windows" aria-controls="Windows" role="tab" data-toggle="tab">Windows</a></li>
      <li role="presentation"><a data-os="macos" href="#editor-macos" aria-controls="MacOS" role="tab" data-toggle="tab">MacOS</a></li>
      <li role="presentation"><a data-os="linux" href="#editor-linux" aria-controls="Linux" role="tab" data-toggle="tab">Linux</a></li>
    </ul>

    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="editor-windows">
        <p>
          nano is a basic editor and the default that instructors use in the workshop.
          It is installed along with Git.
        </p>
        <p>
          Others editors that you can use are
          <a href="https://notepad-plus-plus.org/">Notepad++</a> or
          <a href="https://www.sublimetext.com/">Sublime Text</a>.
          <strong>Be aware that you must
            add its installation directory to your system path.</strong>
          Please ask your instructor to help you do this.
        </p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="editor-macos">
        <p>
          nano is a basic editor and the default that instructors use in the workshop.
          See the Git installation <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">video tutorial</a>
          for an example on how to open nano.
          It should be pre-installed.
        </p>
        <p>
          Others editors that you can use are
          <a href="https://www.barebones.com/products/bbedit/">BBEdit</a> or
          <a href="https://www.sublimetext.com/">Sublime Text</a>.
        </p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="editor-linux">
        <p>
          nano is a basic editor and the default that instructors use in the workshop.
          It should be pre-installed.
        </p>
        <p>
          Others editors that you can use are
          <a href="https://wiki.gnome.org/Apps/Gedit">Gedit</a>,
          <a href="https://kate-editor.org/">Kate</a> or
          <a href="https://www.sublimetext.com/">Sublime Text</a>.
        </p>
      </article>
    </div>
  </div>
</div> {% comment %} End of 'editor' section. {% endcomment %}

<div id="python"> {% comment %} Start of 'Python' section. Remove the third paragraph if
  the workshop will teach Python using something other than
  the Jupyter notebook.
  Details at https://jupyter-notebook.readthedocs.io/en/stable/notebook.html#browser-compatibility {% endcomment %}
  <h3>Python</h3>

  <p>
    <a href="https://python.org">Python</a> ist eine beliebte Sprache für die Verarbeitung von Forschungsdaten und eignet sich auch hervorragend für allgemeine Programmieraufgaben. Die Einzelinstallation aller Forschungspakete kann etwas schwierig sein, daher empfehlen wir <a href="https://www.anaconda.com/distribution/">Anaconda</a>, einen All-in-One-Installer.
  </p>

  <p>
    Unabhängig davon, wie Sie sich für die Installation entscheiden, stellen Sie bitte sicher, dass Sie Python Version 3.x</strong> installieren (z.B. 3.6 ist in Ordnung).
  </p>

  <p>
    Wir unterrichten Python mit dem <a href="https://jupyter.org/">Jupyter Notebook</a>, eine Programmierumgebung, die in einem Webbrowser läuft. Damit dies funktioniert, benötigen Sie einen aktuellen Browser. Die aktuellen Versionen der Chrome, Safari und der Firefox-Browser werden alle <a href="https://jupyter-notebook.readthedocs.io/en/stable/notebook.html#browser-compatibility">unterstützt</a> (einige ältere Browser, einschließlich Internet Explorer Version 9 und älter, werden nicht unterstützt).
  </p>

  <div>
    <ul class="nav nav-tabs nav-justified" role="tablist">
      <li role="presentation" class="active"><a data-os="windows" href="#python-windows" aria-controls="Windows" role="tab" data-toggle="tab">Windows</a></li>
      <li role="presentation"><a data-os="macos" href="#python-macos" aria-controls="MacOS" role="tab" data-toggle="tab">MacOS</a></li>
      <li role="presentation"><a data-os="linux" href="#python-linux" aria-controls="Linux" role="tab" data-toggle="tab">Linux</a></li>
    </ul>

    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="python-windows">
        <a href="https://www.youtube.com/watch?v=xxQ0mzZ8UvA">Video Tutorial</a>
        <ol>
          <li>Open <a href="https://www.anaconda.com/download/#windows">https://www.anaconda.com/download/#windows</a> with your web browser.</li>
          <li>Download the Python 3 installer for Windows.</li>
          <li>Install Python 3 using all of the defaults for installation <em>except</em> make sure to check <strong>Add Anaconda to my PATH environment variable</strong>.</li>
        </ol>
      </article>
      <article role="tabpanel" class="tab-pane active" id="python-macos">
        <a href="https://www.youtube.com/watch?v=TcSAln46u9U">Video Tutorial</a>
        <ol>
          <li>Open <a href="https://www.anaconda.com/download/#macos">https://www.anaconda.com/download/#macos</a> with your web browser.</li>
          <li>Download the Python 3 installer for OS X.</li>
          <li>Install Python 3 using all of the defaults for installation.</li>
        </ol>
      </article>
      <article role="tabpanel" class="tab-pane active" id="python-linux">
        <ol>
          <li>Open <a href="https://www.anaconda.com/download/#linux">https://www.anaconda.com/download/#linux</a> with your web browser.</li>
          <li>Download the Python 3 installer for Linux.<br>
            (The installation requires using the shell. If you aren't
            comfortable doing the installation yourself
            stop here and request help at the workshop.)
          </li>
          <li>
            Open a terminal window.
          </li>
          <li>
            Type <pre>bash Anaconda3-</pre> and then press
            <kbd>Tab</kbd>. The name of the file you just downloaded should
            appear. If it does not, navigate to the folder where you
            downloaded the file, for example with:
            <pre>cd Downloads</pre>
            Then, try again.
          </li>
          <li>
            Press <kbd>Return</kbd>. You will follow the text-only prompts. To move through
            the text, press <kbd>Spacebar</kbd>. Type <code>yes</code> and
            press enter to approve the license. Press enter to approve the
            default location for the files. Type <code>yes</code> and
            press enter to prepend Anaconda to your <code>PATH</code>
            (this makes the Anaconda distribution the default Python).
          </li>
          <li>
            Close the terminal window.
          </li>
        </ol>
      </article>
    </div>
  </div>
  {% comment %}
  <p>
    Wenn Sie mit der Installation der oben aufgeführten Software fertig sind, gehen Sie bitte auf <a href="setup/index.html">diese Seite</a>, die Anweisungen enthält, wie Sie testen können, ob alles korrekt installiert wurde.
  </p>
  {% endcomment %}
</div> {% comment %} End of 'Python' section. {% endcomment %}

<div id="openrefine"> {% comment %} Start of 'OpenRefine' section. {% endcomment %}
  <h3>OpenRefine</h3>
  <p>
    Für diese Lektion benötigen Sie <em>OpenRefine</em> und einen Webbrowser. <em>Hinweis:</em> Dies ist ein Java-Programm, das auf Ihrem Rechner läuft (nicht in der Cloud). Es läuft in einem Webbrowser, aber es wird keine Internetverbindung benötigt. 
  </p>

  <div>
    <ul class="nav nav-tabs nav-justified" role="tablist">
      <li role="presentation" class="active"><a data-os="windows" href="#openrefine-windows" aria-controls="Windows" role="tab" data-toggle="tab">Windows</a></li>
      <li role="presentation"><a data-os="macos" href="#openrefine-macos" aria-controls="MacOS" role="tab" data-toggle="tab">MacOS</a></li>
      <li role="presentation"><a data-os="linux" href="#openrefine-linux" aria-controls="Linux" role="tab" data-toggle="tab">Linux</a></li>
    </ul>

    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="openrefine-windows">
        <p>
          Check that you have either the Firefox or the Chrome browser installed and set as your default browser.
          <strong>OpenRefine runs in your default browser.</strong>
          It will not run correctly in Internet Explorer.
        </p>
        <p>Download software from <a href="http://openrefine.org/">http://openrefine.org/</a></p>
        <p>Create a new directory called OpenRefine.</p>
        <p>Unzip the downloaded file into the OpenRefine directory by right-clicking and selecting "Extract ...". </p>
        <p>Go to your newly created OpenRefine directory.</p>
        <p>Launch OpenRefine by clicking <code>openrefine.exe</code> (this will launch a command prompt window, but you can ignore that - just wait for OpenRefine to open in the browser).</p>
        <p>If you are using a different browser, or if OpenRefine does not automatically open for you, point your browser at <a href="http://127.0.0.1:3333/">http://127.0.0.1:3333/</a> or <a href="http://localhost:3333">http://localhost:3333</a> to use the program.</p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="openrefine-macos">
        <p>Check that you have either the Firefox or the Chrome browser installed and set as your default browser. <strong>OpenRefine runs in your default browser.</strong> It may not run correctly in Safari.</p>
        <p>Download software from <a href="http://openrefine.org/">http://openrefine.org/</a>.</p>
        <p>Create a new directory called OpenRefine.</p>
        <p>Unzip the downloaded file into the OpenRefine directory by double-clicking it.</p>
        <p>Go to your newly created OpenRefine directory.</p>
        <p>Launch OpenRefine by dragging the icon into the Applications folder.</p>
        <p>Use <code>Ctrl-click/Open ... </code> to launch it.</p>
        <p>If you are using a different browser, or if OpenRefine does not automatically open for you, point your browser at <a href="http://127.0.0.1:3333/">http://127.0.0.1:3333/</a> or <a href="http://localhost:3333">http://localhost:3333</a> to use the program.</p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="openrefine-linux">
        <p>Check that you have either the Firefox or the Chrome browser installed and set as your default browser. <strong>OpenRefine runs in your default browser.</strong></p>
        <p>Download software from <a href="http://openrefine.org/">http://openrefine.org/</a>.</p>
        <p>Make a directory called OpenRefine.</p>
        <p>Unzip the downloaded file into the OpenRefine directory.</p>
        <p>Go to your newly created OpenRefine directory.</p>
        <p>Launch OpenRefine by entering <code>./refine</code> into the terminal within the OpenRefine directory.</p>
        <p>If you are using a different browser, or if OpenRefine does not automatically open for you, point your browser at <a href="http://127.0.0.1:3333/">http://127.0.0.1:3333/</a> or <a href="http://localhost:3333">http://localhost:3333</a> to use the program.</p>
      </article>
    </div>
  </div>
</div> {% comment %} End of 'OpenRefine' section. {% endcomment %}

{% comment %}
<div id="vm">
  <h3>Virtual Machine</h3>

  <p>
    Einige Workshop-Instruktoren ziehen es vor, dass die Lernenden eine virtuelle Maschine (VM) verwenden anstatt Software auf ihren eigenen Computern zu installieren.  Wenn sich Ihre Instruktoren dafür entschieden haben, bitte:
  </p>
  <ol>
    <li>
      Installieren Sie <a href="https://www.virtualbox.org/">VirtualBox</a>.
    </li>
    <li>
      Laden Sie unser <a href="{{site.swc_vm}}}">VM-Bild</a> herunter.
      <strong>Warnung:</strong> diese Datei ist 1,7 GByte groß, also bitte Laden Sie es herunter <em>vorher</em> zu Ihrem Workshop zu kommen.
    </li>
    <li>
      Laden Sie die VM in die VirtualBox, indem Sie "Import Appliance" wählen und Laden der Datei <code>.ova</code>.
    </li>
  </ol>
</div>
{% endcomment %}

