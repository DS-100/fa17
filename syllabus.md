---
layout: page
title: "Syllabus"
page_class: content-wide
---

This syllabus is still under development and is subject to change.


<table class="syllabus">
  <colgroup>
    <col width="65px">
    <col width="78px">
    <col width="115px">
    <col width="">
  </colgroup>
  <thead>
    <tr class="syllabus__header">
      <th> Week </th>
      <th> Lecture </th>
      <th> Date </th>
      <th> Topic </th>
    </tr>
  </thead>
  <tbody>

  <!--
  The actual lectures.  Dates are rendered automatically using Jekyll
   -->

  {% include syllabus_entries.html %}

  </tbody>
</table>


<!--

A little script to highlight the week that is next

There is currently a bug in this script which someone needs to fix.  When I wrote this script for my graduate seminar class we only had one lecture a week. We should modify the Jekyll code to render the syllabus with each row tagged so we can automatically identify the week and lecture day.

-->



<script type="text/javascript">
const current_date = new Date();
const lectures = document.getElementsByClassName('lecture');

for (let lecture of lectures) {
  const { lectureWeek, lectureDate } = lecture.dataset;
  const lec_date = new Date(lectureDate + ' 23:59:00');
  if (current_date <= lec_date) {
    lecture.className += ' lecture--current';

    // Need to look up the week element since it might be in the row above
    const weekEl = document.getElementById(`lecture-week-${lectureWeek}`);
    weekEl.className += ' lecture__week--current'
    break;
  }
}

// for (var i = 1; i < rows.length && !finished; i++) {
//   var r = rows[i];
//   if (r.id.startsWith("counter_")) {
//     var fields = r.id.split("_")
//     var week_div_id = "week_" + fields[2]
//     var lecture_date = new Date(fields[1] + " 23:59:00")
//     if (current_date <= lecture_date) {
//       finished = true;
//       r.style.background = "orange"
//       r.style.color = "black"
//       var week_td = document.getElementById(week_div_id)
//       week_td.style.background = "#043361"
//       week_td.style.color = "white"
//     }
//   }
// }
</script>

