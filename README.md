# hw2 part-1

<!DOCTYPE html>
<html>

<head>
    <title>Page Title</title>



</head>

<body>
    <div class="root-container">
        <div class="header">
            <button id="reverse"> 
                REVERSE
            </button>
            <button id="remove-symbols-numbers"> 
                REMOVE SYMBOLS & NUMBERS
            </button>
            <button id="sort-alphabetically"> 
                SORT ALPHABETICALLLY
            </button>
            <button id="color"> 
                TOGGLE COLOR
            </button>
            <button id="random"> 
                RANDOM COLOR
            </button>
            <button id="convert">
                CONVERT TO INLINE
            </button>
        </div>
        <div class="main">
            <div class="startups-container">

            </div>

        </div>
        <div class="footer">

        </div>

    </div>
</body>

</html>

<style>
    .root-container {
        position: relative;
    }

    .root-container .header {
        position: relative;
    }

    .root-container .main {
        position: relative;
    }

    .root-container .footer {
        position: relative;
    }

    .startups-container {
        background-color: gray;
    }

    .red {
        background-image: red;
    }

    .blue {
        background-image: blue;
    }

    .gold {
        background-image: gold;
    }
</style>

<script>
    var colors = ['red', 'blue', 'gold'];
    var chicagoStartupsHTML = [];
    var chicagoStartups = [
        '  Interior   Define  ',
        'Classkick',
        'teaBOT  .$',
        'Pritzker Group Venture Capital',
        'Teln!yx !!',
        'ShipBob ~~$$$',
        'Hologram',
        'Tovala    ',
        '    MANOR',
        'ShuttleCloud 999987',
        'gtrot @@@@@',
        'DealsGoRound ****',
        ' Groovebug',
        'Stage$$$Bloc',
        'Shiftgig',
        'ParkWhiz'
    ];
    

    //HOMEWORK 2 PROBLEMS START
    // 1.CREATE A FUNCTION THAT REVERSES THE LIST OF STARTUPS ON CLICK OF THE REVERSE BUTTON



document.getElementById('reverse').addEventListener('click', function () {

chicagoStartups.reverse();
var list = chicagoStartups;

for (var item in list) {
//create new div and add some value
    var newDiv = document.createElement('div');
    newDiv.id = list[item]; 
    newDiv.className = "list";
    newDiv.innerHTML = list[item];
//add var elements
    document.body.appendChild(newDiv);
	
}
	
});




    // 2.CREATE A FUNCTION THAT REMOVES ALL SYMBOLS AND NUMBERS FROM COMPANY NAMES ON CLICK OF REMOVE SYMBOLS & NUMBERS BUTTON 
    //   Stage$$$Bloc => StageBloc


document.getElementById('remove-symbols-numbers').addEventListener('click', function () {


chicagoStartups = chicagoStartups.toString();
var onlyLetter = chicagoStartups.replace (/[^A-Za-z,' ']+/g, '');

var list = [onlyLetter];

for (var item in list) {
//create new div and add some value
    var newDiv = document.createElement('div');
    newDiv.id = list[item]; 
    newDiv.className = "list";
    newDiv.innerHTML = list[item];
//add var elements
    document.body.appendChild(newDiv);
	
}
	
});








    // 3.CREATE A FUNCTION THAT SORTS STARTUPS IN ALPHABETICAL ORDER ON CLICK OF THE SORT BUTTON



document.getElementById('sort-alphabetically').addEventListener('click', function () {

chicagoStartups.map(function(s) {return String.prototype.trim.apply(s); });

var list = chicagoStartups.sort();


for (var item in list) {
//create new div and add some value
    var newDiv = document.createElement('div');
    newDiv.id = list[item]; 
    newDiv.className = "list";
    newDiv.innerHTML = list[item];
//add var elements
    document.body.appendChild(newDiv);
	
}
	
});







    // 4.CREATE A FUNCTION THAT TOGGLES THE BACKGROUND COLOR UPON CLICK OF THE TOGGLE COLOR BUTTON


document.getElementById('color').addEventListener('click', function () {


document.body.style.backgroundColor='yellow';

	
	
});



    // 5.CREATE A FUNCTION THAT RANDOMLY SELECTS A COLOR CLASS AND APPLIES IT TO EACH COMPANY NAME WHEN THE COLOR BUTTON IS CLICKED




    // 6.CREATE A FUNCTION THAT DISPLAYS STARTS AS INLINE ELEMENTS ON CLICK OF CONVERT TO INLINE BUTTON

document.getElementById('convert').addEventListener('click', function () {



chicagoStartups =chicagoStartups.toString();
var list = [chicagoStartups];

for (var item in list) {
//create new div and add some value
    var newDiv = document.createElement('div');
    newDiv.id = list[item]; 
    newDiv.className = "list";
    newDiv.innerHTML = list[item];
//add var elements
    document.body.appendChild(newDiv);
	
}
	
});





    //HOMEWORK 2 PROBLEMS END

</script>


