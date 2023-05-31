# oibsip_taskono.3
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edges">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <title>temperture converter</title>
    <style>
        body{
            background-color: blanchedalmond;
            padding: 50px 100px;
        }
        h1{
            text-align: center;
        }
        #container{
            text-align: center;
            background-color: lightblue;
            padding:50px;
        }
        .input-div{
            display: inline-block;
        }
        .inp{
            padding: 5px 10px;
            margin: 10px;
            font-size: 30px;
            font-weight: bold;
            color: black;
            width: 150px;
            text-align:center ;
            
        }
        label{
            font-size: 22px;
            color: black;
        }

    </style>
</head>
<body>
   <h1> Temperture converter</h1>
   <div id="container">
        <div class="input-div">
            <label> celsius </label><br>
            <input type="number" value="0" id="cel" class="inp">
        </div>
        <div class="input-div">
            <label> fahernite </label><br>
            <input type="number" value="32" id="fah" class="inp">
        </div>
   </div>
   
    <script>
        var cel = document.getElementById("cel");
        var fah = document.getElementById("fah");

        cel.addEventListener('input',function(){
            let c=this.value;
            let f=(c*9/5)+32;
            if(!Number.isInteger(f)){
                f = f.toFixed(1);
            }
            fah.value=f;
           
        });
        fah.addEventListener('input',function(){
            let f=this.value;
            let c=(f-32)*5/9;
            if(!Number.isInteger(c)){
                c = c.toFixed(4);
            }
            cel.value=c;
        });
    </script> 
</body>
</html>
