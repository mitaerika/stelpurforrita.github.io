---
title: Structure, Agenda, and Schedule
layout: page
description: Schedule and structure of the Stelpur Forrita workshop
bodyClass: page-about
---

# Structure and Agenda 

![Stelpur Forrita aims to assist women and genderqueer individuals in exploring interesting topics in computer science and software enginneering](/images/illustrations/creative_collab.svg)

The structure of the Stelpur Forrita workshop is largely inspired by the success of Nanna Kristjánsdóttir's [Stelpur Diffra workshop](https://www.stelpurdiffra.is/).

Each day, a different theme is explored. The day will start with an introduction to the instructor(s) of the day, then the materials will be explored with a presentation, quizzes, and exercises. The general agenda can be found below:

### Day 1: Introduction, mingling
#### with Ada, Nörd, and sys/tur student representatives
- Topics: Software development as collaborative work, GitHub
- Lunch provided by Arion Bank

### Day 2: E-Commerce
#### with Valenttina Griffin
- Topics: Project management, web development, bringing ideas to reality
- Lunch provided by Arion Bank
- Company visit to Tegra (optional attendance)

### Day 3: Cybersecurity
#### with Jacky Mallet
- Lunch provided by Arion Bank
- Company visit to Keystrike (optional attendance)

### Day 4: AI (Language Technology)
#### with Steinunn Rut Friðriksdóttir
- Topics: Natural Language Processing, life in academia
- Lunch provided by Arion Bank

### Day 5: Career paths post graduation
#### with Safa Jemai
- Topics: Entrepreneurship, hackathon, startup competition, employment
- Lunch presentation at CCP
- Company visit to RB, closing ceremony

# Schedule

In 2024, Stelpur Forrita is scheduled to take place on the following:

**Date:** 12-16 August 2024

**Time:** 09:00-16:00 + company visit time (optional attendance)

**Location:** University of Iceland (Háskóli Íslands) campus, Setberg and Gróska building (see timetable).

<mark> Setberg building (3rd floor), Suðurgata 43, 102 Reykjavík</mark>
![Setberg building at the University of Iceland](/images/locations/setberg.jpg)


<mark style="background: #BDF7D6!important"> Gróska building (3rd floor, Computer Science department), Bjargargata 1, 102 Reykjavík </mark>
![Gróska building at the University of Iceland](/images/locations/groska.png)

**Timetable:**

<script>
  document.addEventListener('DOMContentLoaded', function() {
    var calendarEl = document.getElementById('calendar');
    var calendar = new FullCalendar.Calendar(calendarEl, {
      initialView: 'timeGridWeek',
      weekends: false,
      allDaySlot: false,
      locale: 'is',
      initialDate: '2024-08-12',
      headerToolbar:{
        start: 'prev,next',
        center: 'title',
        end: 'timeGridWeek,timeGridDay',
      },
      titleFormat: {
        month: 'long',
        day: 'numeric',
      },
      dayHeaderFormat:{
        weekday: 'short',
        day: 'numeric',
        month: 'short',
      },
      slotMinTime:'09:00:00',
      slotMaxTime:'18:30:00',
      slotLabelFormat: {
        hour12: false,
        hour: '2-digit',
        minute: '2-digit',
        omitZeroMinute: false,
      },
      visibleRange: {
        start: '2024-08-12',
        end: '2024-08-16',
      },
      events: [
        {% for event in site.data.events %}
          {
            title: '{{ event.title }}',
            start: '{{ event.start }}',
            end: '{{ event.end }}',
            url: '{{ event.url }}',
            backgroundColor: '{{ event.color }}'
          }
          {% unless forloop.last %},{% endunless %}
        {% endfor %}
      ],
      eventTextColor: 'black',
    });
    calendar.render();
  });

</script>

<div id="calendar"></div>
<br>
<p>Color coded locations and details:</p>

<p style="background: #FFFF00">Setberg</p>
<p style="background: #FF9D85">Háskólinn í Reykjavík?</p>
<p style="background: #BDF7D6">Gróska</p>
<p style="background: #1A6EF4">Optional attendance</p>
