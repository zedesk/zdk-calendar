zdk-calendar
============

A simple mini calendar component.

The component uses the [polymer library](http://www.polymer-project.org).

To use it :

    bower install zdk-calendar -S

and include in your html header :

    <script src="/bower_components/webcomponentsjs/webcomponentsjs.min.js"></script>
    <link rel="import" href="/bower_components/zdk-calendar/zdk-calendar.htm">

then to use it, insert in the body of your html file :

    <zdk-calendar></zdkcalendar>

the component expose the following attributes :

  - i18n : The language setting for the calendar
  - date : The date of the calendar ( by default today )
  - start : sets the first selectable date 
  - stop : sets the last selectable date
  - selected : the selected date

the component emits one event : "select" when clicking on a date. The event come with the following object :

    {
        "day": "15/05/2014",      // A string represenation of the selected date in the selected language setting
        "time": 1400104800000     // the timestamp of the selected date
    }   


## zdk-input-date

This component create a custom input component that use the calendar to fill-up dates.

    <script src="/bower_components/webcomponentsjs/webcomponentsjs.min.js"></script>
    <link rel="import" href="/bower_components/zdk-calendar/element.htm">

then to use it, insert in the body of a form :

    <zdk-input-date name="stardate" value="2014-12-15"></zdk-inpuut-date>

to collect form results, i used a modified version of [`form2js`](https://github.com/maxatwork/form2js), see form2js in the sources

