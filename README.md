Date time picker integrated the Pytholabs page
View the README file in a code editor.
STEPS TO INTEGRATE:

1. link css : '<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/jquery-datetimepicker/2.5.20/jquery.datetimepicker.min.css">'
2. link JS (AFTER JQUERY): <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery-datetimepicker/2.5.20/jquery.datetimepicker.full.min.js"></script>
3. Init DATE TIME PICKER : $(document).ready(function(){
    $("#fdate" ).datetimepicker({
        dateFormat: 'yy-mm-dd',
        timeFormat: 'HH:mm:ss',
        onShow: function () {
            this.setOptions({
                maxDate:$('#tdate').val()?$('#tdate').val():false,
                maxTime:$('#tdate').val()?$('#tdate').val():false
            });
        }
  }).attr('readonly', 'readonly');
  $( "#tdate" ).datetimepicker({
      dateFormat: 'yy-mm-dd',
      timeFormat: 'HH:mm:ss',
        onShow: function () {
            this.setOptions({
                minDate:$('#fdate').val()?$('#fdate').val():false,
                minTime:$('#fdate').val()?$('#fdate').val():false
            });
        }                    
  }).attr('readonly', 'readonly'); 

  $("#timedate").click(function(){
      console.log($('#tdate').val());
      console.log($('#fdate').val());
  })    
    
   
});
 4. HTML EXAMPLE:
 <input type="button" value="submit date" id="timedate">

<input placeholder="From Date & Time" id="fdate" type="text"/>
<input placeholder="To Date & Time" id="tdate" type="text"/>


Code Example in datetimepicker.html:

Line(s) 105: Link CSS  ==>> STEP(1)
Line(s) 1630: link JS (AFTER JQUERY)
Line(s) 1631 -1660: INIT DATETIME PICKER
Line(s) 1549 - 1552 : Code Example