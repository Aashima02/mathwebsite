# Web Page for Mathematical Calculations

## AIM:

To design a static website with validation to perform mathematical calculations in client side.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS.

### Step 3:

Write javascript to perform the calculations.

### Step 4:

Include regularexpression based input validation.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Math Website</title>
    <style>
        *{
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}

body{
  background-color: rgb(146, 26, 110);
  color: black;
}

.container{
  width: 1080px;
  margin-left: auto;
  margin-right: auto;
}

.content{
  display: block;
  width: 100%;
  margin-left: auto;
  margin-right: auto;
  background-color: rgb(233, 202, 145);
  margin-top: 35px;
  min-height: 400px;
}

h1{
    color: black;
    text-align: center;
    padding-top: 20px;
}

.formelement{
    text-align: center;
    padding-top: 20px;
    font-size: larger;
}

.footer{
    display: inline-block;
    width: 100%;
    height: 35px;
    background-color: darksalmon;
    color: black;
    text-align: center;
    padding-top: 10px;
    font-size: large;
}

    </style>
</head>
<body>
    <div class="container">
        <div class="content">
            <h1><u>Volume of Cone</u></h1>
            <form>
                <div class="formelement">
                    <label for="redit">Radius:</label>
                    <input type="text" id="redit" value="0"/> Meters
                </div>
                <div class="formelement">
                    <label for="hedit">Height:</label> 
                    <input type="text" id="hedit" value="0"/> Meters
                </div>
                <div class="formelement">
                    <input type="button" value="Calculate Volume" id="volbutton"/>
                </div>
                <div class="formelement">
                    <label for="cedit">Volume:</label> 
                    <input type="text" id="cedit" readonly value="0"/> Meter<sup>3</sup>
                </div>
            </form>
        </div>
    </div>
    <div class="container">
        <div class="content">
            <h1><u>Surface Area of Cylinder</u></h1>
            <form>
                <div class="formelement">
                    <label for="dcyl">Radius:</label>
                    <input type="text" id="dcyl" value="0"/> Meters
                </div>
                <div class="formelement">
                    <label for="bcyl">Height:</label>
                    <input type="text" id="bcyl" value="0"/> Meters
                </div>
                <div class="formelement">
                    <input type="button" value="Calculate Surface Area" id="sabutton"/>
                </div>
                <div class="formelement">
                    <label for="zcyl">Surface Area:</label>
                    <input type="text" id="zcyl" readonly value="0"/> Meter<sup>2</sup>
                </div>
            </form>
        </div>
        <div class="footer">Developed by Aashima Nazreen S</div>
    </div>

<script>
    var button;
    button=document.querySelector("#volbutton");
    button.addEventListener("click",function(){
        var rtext,htext,ctext;
        var rval,hval,cval;
        var result,result1,rexp;
        rtext=document.querySelector("#redit");
        htext=document.querySelector("#hedit");
        ctext=document.querySelector("#cedit");

        rexp=new RegExp("^[1-9]+[0-9]*$");

        rval=rtext.value;
        result=rval.match(rexp);
        hval=htext.value;
        result1=hval.match(rexp);

        if(result==null)
        {
            alert("Please enter only positive integers for Radius");
        }
        if(result1==null)
        {
            alert("Please enter only positive integers for Height")
        }
        cval=((22/7)*rval*rval*hval)/3;
        ctext.value=""+cval;

    });

    var button;
    button=document.querySelector("#sabutton");
    button.addEventListener("click",function(){
        var dtext,btext,ztext;
        var dval,bval,zval;
        var result2,result3,rexp1;
        dtext=document.querySelector("#dcyl");
        btext=document.querySelector("#bcyl");
        ztext=document.querySelector("#zcyl");

        rexp1=new RegExp("^[1-9]+[0-9]*$");

        dval=dtext.value;
        result2=dval.match(rexp1);
        bval=btext.value;
        result3=bval.match(rexp1);

        if(result2==null)
        {
            alert("Please enter only positive integers for Radius");
        }
        if(result3==null)
        {
            alert("Please enter only positive integers for Height");
        }
        zval=2*22/7*dval*(dval+bval);
        ztext.value=""+zval;

    });
</script>
</body>
</html>
```

## OUTPUT:

![screenshot](https://user-images.githubusercontent.com/93427086/149363222-5bca1bad-61bd-4787-9247-ffad9e87b099.png)
![validator](https://user-images.githubusercontent.com/93427086/149363241-6ffe7165-9923-495e-9476-f1a0362c359a.png)

## RESULT:

Thus a website is designed to perform mathematical calculations in the client side.
