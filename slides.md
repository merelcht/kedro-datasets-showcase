---
layout: image
image: background.png
---
<div id="padding" class="mt-5"></div>
<div grid="~ cols-2 gap-4">
<div class="mt-10">
<p class="text-2em text-yellow-500"><span class="bg-dark-900 m-2 mb-0 rounded bg-opacity-60"> Kedro Showcase </span></p><br>

### October 2022


</div>
<div class="w-130"><KedroIcon /></div>

</div>

---
theme: apple-basic
class: text-left
highlighter: shiki
layout: DemoLayout
---

# Today's agenda

We’re excited to show you some of the cool stuff we’re currently cooking up and our vision for the future and Kedro's place within the ML ecosystem.

<ul>
  <li><span @click="$slidev.nav.go(3)" hover="bg-white bg-opacity-10 rounded">🤖 Meet the team</span></li>
  <li><span @click="$slidev.nav.go(4)" hover="bg-white bg-opacity-10 rounded">👩‍🍳 What have the team been cooking?</span></li>
  <li><span @click="$slidev.nav.go(11)" hover="bg-white bg-opacity-10 rounded">🧑‍💻 What has the community been up to?</span></li>
  <li><span @click="$slidev.nav.go(12)" hover="bg-white bg-opacity-10 rounded">💿 Changes to Datasets</span></li>
  <li><span @click="$slidev.nav.go(18)">📣 Feedback + Q&A</span></li>
</ul>

<Socials />

---

# Meet the team

<div class="flex">
  <div class="p-1">
      <div><h3>Placeholder title</h3></div>
      <div class="flex p-2 gap-2">
         <div><Profile name="Ivan" role="Engineering Lead" github="idanov" country="🇧🇬"/></div>
         <div><Profile name="Yetu" role="Product Lead" github="yetudada" country="🇿🇦"/></div>
         <div><Profile name="Nero" role="Product Manager" github="NeroOkwa" country="🇳🇬"/></div>
         <div><Profile name="Jo" role="Tech Writer" github="stichbury" country="🏴󠁧󠁢󠁷󠁬󠁳󠁿"/></div>
     </div>
     </div>

  <div class="p-1">
     <div><h3>Viz team</h3></div>
     <div class="flex p-2 gap-2">
      <div><Profile name="Tynan" role="Tech Lead" github="tynandebold" country="🇺🇸"/></div>
      <div><Profile name="Rashida" role="SWE" country="🇮🇳" github="rashidakanchwala"/></div>
      <div><Profile name="Huong" role="SWE" country="🇻🇳" github="Huongg"/></div>
      <div><Profile name="Cvetanka" role="SWE" country="🇲🇰" github="cvetankanechevska"/></div>
      <div><Profile name="Gabriel" role="Design Lead"  country="🇧🇷" github="GabrielComymQB"/></div>
      <div><Profile name="Andrew" role="Product Designer" github="Mackay031" country="🇿🇦"/></div>
  </div></div></div>

  <div class="flex">
  <div class="p-1">
    <div><h3>Framework team</h3></div>
    <div class="flex p-2 gap-2">
      <div><FrameworkProfile name="Merel" role="Tech Lead" github="MerelTheisenQB" country="🇳🇱"/></div>
      <div><FrameworkProfile name="Antony" role="DS SWE" github="AntonyMilneQB" country="🇬🇧"/></div>
      <div><FrameworkProfile name="Nok" role="SWE" github="noklam" country="🇭🇰"/></div>
      <div><FrameworkProfile name="Ahdra" role="SWE" github="AhdraMeraliQB" country="🇰🇪"/></div>
      <div><FrameworkProfile name="Sajid" role="SWE" github="SajidAlamQB" country="🇬🇧"/></div>
      <div><FrameworkProfile name="Ankita" role="SWE" github="ankatiyar" country="🇮🇳"/></div>
      <div><FrameworkProfile name="Jannic" role="SWE" github="jmholzer" country="🇬🇧"/></div>
      <div><FrameworkProfile name="Deepyaman" role="DS SWE" github="deepyaman" country="🇺🇸"/></div>
    </div>
    <div class="pb-5"></div>
  </div>
</div>


---

## What have the team been cooking recently 👩‍🍳?

<h3> <br>Since March this year we have released versions <kbd>0.18.0</kbd>, <kbd>0.18.1</kbd>, <kbd>0.18.2</kbd>, and <kbd>0.18.3</kbd> 🎉<br>
Here's a look at some of the things we've done:</h3>
<div class="grid grid-cols-4 mt-3">

  <div class="w-50 m-2">
    <div class="bg-dark-400 rounded-lg flex flex-col content-between  ">
      <emojione-building-construction class="text-3em m-auto mt-2 -mb-2 h-10"/>
      <p class="text-center text-0.8em text-white opacity-90">
        Rewritten framework internals
      </p>
    </div>
  </div>

  <div class="w-50 m-2">
    <div class="bg-dark-400 rounded-lg flex flex-col content-between ">
      <logos-python class="text-3em m-auto mt-2 -mb-2 h-10"/>
        <p class="text-center text-0.8em text-white opacity-90">
          Support for Python 3.9 & 3.10
        </p>
    </div>
  </div>

  <div class="w-50 m-2">
    <div class="bg-dark-400 rounded-lg flex flex-col content-between ">
        <iconoir-packages class="text-3em m-auto mt-2 -mb-2 h-10 text-purple-400"/>
        <p class="text-center text-0.8em text-white opacity-90">
          Micropackaging workflow
      </p>
    </div>
  </div>

  <div class="w-50 m-2">
    <div class="bg-dark-400 rounded-lg flex flex-col content-between">
      <vaadin-file-tree-sub class="text-3em m-auto mt-2 -mb-2 h-10 text-blue-400"/>
        <p class="text-center text-0.8em text-white opacity-90">
          Improved interactive workflow
        </p>
    </div>
  </div>

</div>


<div class="grid grid-cols-4">
  <div class="w-50 m-2">
    <div class="bg-dark-400 rounded-lg flex flex-col content-between ">
     <mdi-hook class="text-3em m-auto mt-2 -mb-2 h-10 text-green-400"/>
        <p class="text-center text-0.8em text-white opacity-90">
          Added hooks
        </p>
    </div>
  </div>

  <div class="w-50 m-2">
    <div class="bg-dark-400 rounded-lg flex flex-col content-between ">
     <ant-design-file-search-outlined class="text-3em m-auto mt-2 -mb-2 h-10 text-blue-200"/>
        <p class="text-center text-0.8em text-white opacity-90">
          Pipeline autodiscovery
        </p>
    </div>
  </div>

  <div class="w-50 m-2">
    <div class="bg-dark-400 rounded-lg flex flex-col content-between ">
      <carbon-terminal class="text-3em m-auto mt-2 -mb-2 h-10 text-orange-400"/>
        <p class="text-center text-0.8em text-white opacity-90">
          Rich logs
        </p>
    </div>
  </div>

  <div class="w-50 m-2">
    <div class="bg-dark-400 rounded-lg flex flex-col content-between ">
      <mdi-graph-outline class="text-3em m-auto mt-2 -mb-2 h-10 text-pink-400"/>
        <p class="text-center text-0.8em text-white opacity-90">
          Export runs from Viz
        </p>
    </div>
  </div>

</div>

<div class="grid grid-cols-4">
  <div class="w-50 m-2">
    <div class="bg-dark-400 rounded-lg flex flex-col content-between ">
    <codicon-graph class="text-3em m-auto mt-2 -mb-2 h-10 text-red-400"/>
      <p class="text-center text-0.8em text-white opacity-90">
        Plots in experiment tracking
      </p>
    </div>
  </div>

  <div class="w-50 m-2">
    <div class="bg-dark-400 rounded-lg flex flex-col content-between">
     <div class="text-3em m-auto mt-2 -mb-2 h-10 text-gray-100"> <img class="w-10 h10" src="/public/kedroid.png"/> </div>
        <p class="text-center text-0.8em text-white opacity-90">
          New website
        </p>
    </div>
  </div>

  <div class="w-50 m-2">
    <div class="bg-dark-400 rounded-lg flex flex-col content-between">
      <logos-slack-icon class="text-3em m-auto mt-2 -mb-2 h-10"/>
      <p class="text-center text-0.8em text-white opacity-90">
        Kedro on Slack
      </p>
    </div>
  </div>

  <div class="w-50 m-2">
    <div class="bg-dark-400 rounded-lg flex flex-col content-between ">
      <emojione-bug class="text-3em m-auto mt-2 -mb-2 h-10"/>
        <p class="text-center text-0.8em text-white opacity-90">
          Dead bugs
        </p>
    </div>
  </div>

</div>


<Socials />

---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080 #placeholder
---
<p class="text-1.3em"> <vaadin-file-tree-sub class=" m-auto mr-5 ml-2 text-blue-400"/> Improved interactive workflow</p>

<style>
  li {
    font-size: 0.8em;
    list-style-type: circle;
  }
</style>

<div id="padding" class="m-8">
</div>

- The only recommended way to work with Kedro in Jupyter or IPython is now the Kedro IPython extension.

- Managed Jupyter instances should load this via `%load_ext kedro.ipython` and use the line magic `%reload_kedro`.

- `kedro ipython` launches an IPython session that preloads the Kedro IPython extension.

- `kedro jupyter notebook/lab` creates a custom Jupyter kernel that preloads the Kedro IPython extension and launches a notebook with that kernel selected.

- The Kedro IPython extension also works with Databricks notebooks. 


<Socials />

---
layout: image-right
image: #none
---

<p class="text-1.3em"> <ant-design-file-search-outlined class=" m-auto mr-5 ml-2 text-blue-200"/> Pipeline autodiscovery</p>

<style>
  li {
    list-style-type: circle
  }
</style>

<div id="padding" class="m-20">
</div>

- Pipelines, once created, are now registered automatically.
<br>
<br>
- No need to explicitly add it to the pipeline registry to access it by name (e.g. `kedro run --pipeline=<pipeline_name>`) or through the default pipeline (e.g. `kedro run`).

<Socials />

---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080 #placeholder
---

<p class="text-1.3em"> <carbon-terminal class=" m-auto mr-5 ml-2 text-orange-400"/> Rich logs</p>

<style>
  li {
    list-style-type: circle;
  }
</style>

<div id="padding" class="m-20">
</div>

- Rich is an amazing, open-source library that superpowers the terminal experience.
<br>
<br>

- Kedro now supports Rich logging, which turns our logs and tracebacks from boring and hard-to-read to pretty and colourful 🌈
- We're not done yet! Expect more Rich-related changes to come soon.

<Socials />
---
layout: DemoLayout
---

<p class="text-1.3em"> <codicon-graph class=" m-auto mr-5 ml-2 text-red-400"/> Plots on Experiment Tracking</p>

<style>
  li {
    list-style-type: circle
  }
</style>

<div id="padding" class="mt-20 mr-7">

- In the last year we released experiment tracking on Kedro-Viz 📈 🎉
<br>
<br>

- As part of this, you can now see your plots within the experiment tracking view to compare them side-by-side
<br>
<br>

- Visit our docs for a walkthrough on adding this functionality

</div>

<Socials />

---
layout: iframe-right
url: https://kedro.org/
---
<div class="pt-3" style="display:flex; vertcal-align:text-bottom">
  <span style="display:inline-block; font-size:1.3em;">
  <img class="m-auto mr-5 ml-2 w-7 h10" style="display:inline; vertical-align:bottom" src="/public/kedroid.png"/> New Website</span>
</div>

<style>
  li {
    list-style-type: circle
  }
</style>

<div id="padding" class="m-15">
</div>

- We've now got our very own Kedro website! 
<br>

- This is our online home and a centralised hub for all things Kedro. 
<br>

- Here you can find our documentation, tutorials, and links to our online forums where you can join our Kedro community. Check it out!

<Socials />

---

<p id="heading" class="text-1.3em"> <logos-slack-icon class=" m-auto mr-5 ml-2"/> Kedro on Slack</p>

<style>

  #main {
    font-size: 0.8em;
    text-align: center;

  }
  li {
    list-style-type: circle
  }
</style>

<div id="padding" class="m-6">
</div>

<img src="https://demo.kedro.org" alt="Kedro slack invite QR code" class="w-60 h-60"/>

<p id="main">
We have launched a Kedro Slack organisation, and you should join it

You'll be able to collaborate and learn from our 800+ member open-source community that we will also migrate to this new location. Join the new Slack organisation 🎉
</p>


<Socials />

<!--
Mention Hacktoberfest
-->

---

# Placeholder slide - What has the community been up to?

<Socials />
---
layout: image-right
---

# Changes to datasets

<style>
  li {
    list-style-type: circle
  }
</style>

<div id="padding" class="m-15">
</div>

- Datasets are Kedro's way of dealing with input and output in a data and machine-learning pipeline. 


- Kedro supports many datasets out of the box to allow you to process different data formats including Pandas, Plotly, Spark and many more.
  
- These datasets have lived in Kedro within `kedro/extras/datasets`


<Socials />
---
layout: image-right
---

# The Problem

<style>
  li {
    list-style-type: circle
  }
</style>

<div id="padding" class="mt-8">


- Kedro's dependency on these datasets has added additional constraints that affect our workflow

- For example:
  <div class="text-0.9em">

  - We couldn't add Python 3.9 and 3.10 support to the Kedro framework until all of our datasets had also released Python 3.9 and 3.10 support.

  - We couldn't provide new, but workflow-breaking, dataset functionality as the Kedro framework versioning is more conservative than the datasets.
  </div>

</div>

<Socials />
---
layout: image-right
---

# Our Solution

<style>
  li {
    list-style-type: circle
  }
</style>

<div id="padding" class="m-8">
</div>

We want to move the datasets out into a separate package, `kedro-datasets`.

This means:

- Kedro becomes more modular, making it possible for users to upgrade only the kedro-datasets dependency in production rather than modifying the entire template.
  
- Users can leverage newer datasets with older versions of Kedro and can use datasets without Kedro.



<Socials />
---
layout: two-cols
---

# What do these changes mean for you?

There are three main changes to be aware of:

1.  In addition to installing Kedro, users will need to install `kedro-datasets` to make use of datasets. 
   <br>


::right::
<div class="m-10 p-5 text-1.5em h-30">

Old workflow 🙅
<br>
<br>

```bash
pip install kedro[SomeDataSet]
```
</div>
<div class="m-10 p-5 text-1.5em">
New workflow ✅
<br>
<br>

```bash
pip install kedro-datasets[SomeDataSet] 
```
</div>

<Socials />
---
layout: two-cols
---

# What do these changes mean for you?

There are three main changes to be aware of:

1.  In addition to installing Kedro, users will need to install kedro-datasets to make use of datasets. 
   <br>
   <br>

2.  Importing the datasets will look different.


::right::
<div class="m-10 p-5 text-1.5em h-30">

Old workflow 🙅
<br>
<br>

```py
from kedro.extras.datasets import SomeDataSet
```
</div>
<div class="m-10 p-5 text-1.5em">
New workflow ✅
<br>
<br>

```py
from kedro_datasets import SomeDataSet
```
</div>

<Socials />
---
layout: two-cols
---

# What do these changes mean for you?

There are three main changes to be aware of:

1.  In addition to installing Kedro, users will need to install kedro-datasets to make use of datasets. 
   <br>
   <br>

2.  Importing the datasets will look different.
   <br>
   <br>

3.  Any dataset contributions should be made to `kedro-datasets` (part of the `kedro-plugins` repository), not core `kedro`.

::right::
<div class="m-10 p-5 text-1.5em h-30">

Old workflow 🙅
<br>
<br>

```py
from kedro.extras.datasets import SomeDataSet
```
</div>
<div class="m-10 p-5 text-1.5em">
New workflow ✅
<br>
<br>

```py
from kedro_datasets import SomeDataSet
```
</div>

<Socials />
---
layout: quote
---
# 📣 Feedback + Q&A Session

<div abs class=" abs-tr mr-60 mt-52">
<img src="/questions.gif" class="rounded rounded-lg shadow-lg h-30"/>
</div>
<Socials />
