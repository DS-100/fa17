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
  The actual lecture rows. To add a lecture, edit _data/lectures.yml.
   -->

  {% include syllabus_entries.html %}

  </tbody>
</table>

<!--
Script to highlight the current lecture.
-->

<script type="text/javascript">
const current_date = new Date();
const lectures = document.getElementsByClassName('lecture');

for (var i = 0; i < lectures.length; i++ ) {
  let lecture = lectures[i]
  const { lectureWeek, lectureDate } = lecture.dataset;
  const lec_date = new Date(lectureDate + ' 23:59:00');
  if (current_date <= lec_date) {
    lecture.className += ' lecture--current';

    // Need to look up the week element since it might be in the row above
    const weekEl = document.getElementById(`lecture-week-${lectureWeek}`);
    weekEl.className += ' lecture__week--current';
    window.location.hash = `lecture-week-${lectureWeek}`;
    break;
  }
  
}
</script>

