<!-- .slide: data-state="section-break" id="maintenance" data-timing="20" -->
# Life after creating your project

Note:
A lot of the stuff in this section are general best practice
principles for any project not just OpenStack projects, so
I'll try to focus on the specific differences in the OpenStack
ecosystem.


<!-- .slide: data-state="normal" id="thumb-up" data-timing="20" -->
## Code review

<div style="height: 80%; float: left">
<img alt="thumbs up"
         data-src="images/thumbs-up.jpg" />
</div>
<figure class="fragment" style="float: right; width: 50%">
    <img alt="thumb down"
         data-src="images/thumb-down.jpg" />
     <figcaption>
         <a href="https://commons.wikimedia.org/wiki/File:Disapprove.jpg">
             &copy; hobvias sudoneighm CC-BY-SA 2.0
         </a>
     </figcaption>
</figure>

Note:
- Firstly be responsive! otherwise project will fail.
- Everyone is familiar with +1, and it's easy to give positive feedback.
- If you want to give a -1, it's a bit more complicated ...


<!-- .slide: data-state="normal" id="constructive-collaboration" data-timing="60" -->
## Constructive collaboration

<figure class="full-slide">
    <img alt="donut burger"
         data-src="images/donut-burger.jpg" />
     <figcaption>
         <a href="https://commons.wikimedia.org/wiki/File:Donut_burger.jpg">
             &copy; Phil Denton CC-BY-SA 2.0
         </a>
     </figcaption>
</figure>

Note:
- In F/OSS world, when you're collaborating with people you've never met,
  you have to tread a bit more carefully.
- "Criticism sandwich" imperfect, but still has value.
- Be positive, welcoming, and open-minded
- Aim to leave contributor wanting to come back


<!-- .slide: data-state="normal" id="core-reviewers" data-timing="30" -->
## Core reviewers

<figure class="full-slide">
    <img alt="two thumbs up"
         data-src="images/two-thumbs-up.jpg" />
     <figcaption>
         <a href="https://commons.wikimedia.org/wiki/File:Young_Somali_man_2.jpg">
             &copy; Entressen kirjasto CC-BY-SA 2.0
         </a>
     </figcaption>
</figure>

<p style="position: absolute; left: 65%; top: 30%; font-size: 7em;">+2</p>

Note:
- When you have created an OpenStack project, you are responsible for
  approving changes for merge via +2, but also who else will be in the
  core reviewer's team with the rights to give +2.  This team will
  probably need membership changes over time.


<!-- .slide: data-state="normal" id="other-votes" data-timing="60" -->
## Other review mechanisms

*   -2: core veto (try to avoid!)
*   +1 workflow: merge it!
*   -1 workflow: draft or WIP
*   0

<p style="margin-top: 2em">
    Reference: [Core Reviewer's Guide](http://docs.openstack.org/infra/manual/core.html)
</p>

<p style="margin-top: 2em">
    https://github.com/openstack/gerrit-dash-creator
</p>

Note:
0 can be a valid vote sometimes, when you are indifferent.


<!-- .slide: data-state="normal" id="CI" data-timing="20" -->
## CI

<img alt="CI status graphs"
     style="height: 80%"
     data-src="images/CI-stats.png" />

Note:

From status.openstack.org, CI results sorted by % failures.
Noone wants to be in hall of shame!  So ensure CI stays healthy and
visible; this will breed confidence in your project.  Always look for
opportunities to improve it.  Passing is not enough - also need good
code coverage!


<!-- .slide: data-state="normal" id="release-management" data-timing="90" -->
## Release Management

<div style="height: auto; float: right; margin-left: 80px">
<img data-src="images/balloon_release.jpg" />
</div>

<ul style="display: inline">
    <li>[SemVer](http://semver.org/) recommended
    <li>Decide a release model
        <ul>
            <li> `release:cycle-with-intermediary` (5.0.0.0b1, 5.0.0.0rc2)
            <li> `release:cycle-with-milestones` (X.Y.Z)
            <li> `release:independent`
        </ul>
    <li>Build / publish tarballs
    <li>Release notes ([`reno`](http://docs.openstack.org/developer/reno/design.html))
    <li>Integrate translations via https://translate.openstack.org/
    <li>http://docs.openstack.org/project-team-guide/release-management.html
</ul>

Note:
If in Big Tent, you are typically expected to follow stable release cycle.


<!-- .slide: data-state="section-break" id="reactive-support" data-timing="10" -->
# Reactive support

Note:
- Providing decent support can mean the difference between
  life and death of the project.


<!-- .slide: data-state="normal" id="bugs" data-timing="20" -->
## Bug / issue tracking

<figure class="full-slide">
    <img alt="A metallic shield bug"
         data-src="images/bug.jpg" />
     <figcaption>
         <a href="https://commons.wikimedia.org/wiki/File:Metallic_shield_bug444.jpg">
             &copy; Benjamint444 CC-BY-SA 3.0
         </a>
     </figcaption>
</figure>

Note:
- launchpad recommended
- triage quickly
- ensure it's always clear what state each issue is in
    - if noone's working on it, that's OK as long as it's clear


<!-- .slide: data-state="normal" id="ML-support" data-timing="20" -->
## Mailing list support

```email
To: <openstack-dev@lists.openstack.org>
Subject: [openstack-dev] [neutron] [L3] Wrong fail over of HA-Router
```

<p style="margin-top: 2em" />

* https://wiki.openstack.org/wiki/Mailing_Lists
* http://lists.openstack.org/

Note:
- as with bugs, make sure mails don't get ignored
- encourage people to use `[tags]` for easier filtering, so you
  don't accidentally miss important mails


<!-- .slide: data-state="normal" id="IRC-channel" data-timing="30" -->
## `#openstack-foo`

- Helpful to set up project channel on FreeNode if there is
  no existing channel suitable for reuse
- Work with infra team
- Register with `chanserv` and set a helpful topic


<!-- .slide: data-state="normal" id="IRC-support" data-timing="20" -->
## IRC support

<figure class="full-slide">
    <img alt="a tumbleweed"
         data-src="images/Tumbleweed_rolling.jpg" />
     <figcaption>
         <a href="https://commons.wikimedia.org/wiki/File:Tumbleweed_rolling.jpg">
             &copy; Jez Arnold CC-BY-SA 2.0
         </a>
     </figcaption>
</figure>

Note:
- In OpenStack, IRC and mailing lists are focal point of daily collaboration.
- At first your project may be "quiet", so watch the channel carefully
  and make sure questions are going answered.


<!-- .slide: data-state="normal" id="gerritbot" data-timing="30" -->
## gerritbot

```text
<openstackgerrit> Adam Spiers proposed openstack/openstack-resource-agents:
                  Clarify risks of not using shared storage
                  https://review.openstack.org/297663
```

```
openstack-ha:
  events:
    - patchset-created
    - change-merged
    - x-vrif-minus-2
  projects:
    - openstack/ha-guide
    - openstack/openstack-resource-agents
  branches:
    - master
```

- http://docs.openstack.org/infra/manual/drivers.html#gerrit-irc-notifications

Note:
One way to avoid embarrassment of total silence is to install a
bot - may seem like cheating, but can actually help people feel
more connected to what's going on in the project.


<!-- .slide: data-state="section-break" id="proactive-support" data-timing="10" -->
# Proactive support

Note:
- reactive support is a good start, but for a project to really
  flourish, it needs a more proactive approach


<!-- .slide: data-state="normal" id="IRC-meetings" data-timing="30" -->
## `#openstack-meeting`

Meetbot!

<img data-src="images/ircmeeting.png" style="width: 100%"/>

* https://wiki.openstack.org/wiki/Meetings
* http://eavesdrop.openstack.org/

Note:
- meetings must be scheduled in one of the existing meeting channels
  in order to minimise clashes with other meetings


<!-- .slide: data-state="normal" id="physical-meetings" data-timing="30" -->
## Physical meetings

<figure class="full-slide">
    <img alt="a meeting"
         data-src="images/meeting.png" />
     <figcaption>
         Credit:
         <a href="http://www.openstack.org/blog/2013/03/introducing-the-openstack-operations-guide/">blog about OpenStack Ops guide
         </a>
     </figcaption>
</figure>

Note:
- personal relationships matter!
- form relationships at summits, mid-cycles, and other meetups


<!-- .slide: data-state="normal" id="proactive-communication" data-timing="60" -->
## Proactive communication

* Documentation
* Interaction with other projects
* Releases
* Blogging
* Mentoring and guiding new contributors
* Training, screencasts etc.
* Gather feedback via PWG / user stories / specs

Note:
- The Cross-project Working Group is available to help with
  topics which span multiple projects.
- Make sure your blog is aggregated to planet.openstack.org!
- Submit user stories / specs and ask for reviews
