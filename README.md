# jspdf

###### jsPDF is very easy for basic PDF files generation

`````

<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/1.0.272/jspdf.debug.js"></script>
    <script type="text/javascript">
        var pdf = new jsPDF();
        pdf.text(30, 30, 'Hello world!');
        pdf.save('hello_world.pdf');
    </script>
<body>
    <h1>Hello world</h1>
    
</body>

`````


#### Export Web Page Into PDF using by jsPDf

``````
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/1.3.3/jspdf.debug.js"></script>
<script src="http://code.jquery.com/jquery-1.10.2.js"></script>
<script src="http://code.jquery.com/ui/1.11.2/jquery-ui.js"></script>

<!--<script>
var doc = new jsPDF()
 
doc.text('Hello world!', 10, 10)
doc.save('a4.pdf')

</script>-->
 <script>
$(document).ready(function (){
                            $('#click').click(function () {
                            var specialElementHandlers = 
                            function (element,renderer) {
                            return true;
                            }
                            var doc = new jsPDF();
                            doc.fromHTML($('#content').html(), 15, 15, {
                            'width': 170,
                            'elementHandlers': specialElementHandlers
                            });
                            doc.output('datauri'); 
                        });
                        });
</script>

<body id="target" >
     <div id="content">
         <h4>Hello, this is a H4 tag</h4>
        <p>a pararaph</p>
     </div>
  <div id="editor"></div>
  <button id="click">generate PDF</button>
</body>

``````
