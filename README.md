# BMI-Calculater
<html>
    <head>
        <title></title>
        <!-- Latest compiled and minified CSS -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">


    </head>
    <body>
        <div class="container">
            <div class="card">
                <div class="card-header text-center">BMI Calculator </div>
                <div class="card-body"> 
                <form class="w-50 m-auto" onsubmit="return fasle">
                    <div class="form-group">
                        <lebel> Weight </lebel>
                        <input type="number" name="" placeholder="Weight in Kg" required id="weight" class="form-control">
                    </div>
                    <div class="form-group">
                        <lebel> Height </lebel>
                        <input type="number" name="" placeholder="Height in Ft" required id="height" class="form-control">
                    </div>
                    <div class="form-group">
                        <lebel> BMI Value </lebel>
                        <input type="number" name="" id="bmivalue" class="form-control">
                    </div>
                    <div>
                        <button type="submit" class="btn btn-success" onclick="getbmivalue()">Check BMI</button>
                    </div>
                </form>   
                </div>
                <div class="card-footer text-center"> A healthy BMI ranges between 19 and 25. </div>
            </div>
        
        </div>


        <script>
            

            function getbmivalue(){
                var weight = document.getElementById('weight').value;
                var height = document.getElementById('height').value;   

                height = height * 12;
                height = height * 0.025; //now height meter

                // var newbmivalue = weight / (height * height);
                var newbmivalue = weight / Math.pow(height,2);
                newbmivalue = Math.round(newbmivalue);

                document.getElementById('bmivalue').value = newbmivalue;

            }
        </script>


        <!-- jQuery library -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>

<!-- Popper JS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.0/umd/popper.min.js"></script>

<!-- Latest compiled JavaScript -->
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script
    </body>
</html>
