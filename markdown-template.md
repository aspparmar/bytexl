-- this file is to contains mark down template and format with embedded html and block i need to create the course work for my lms 

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
  body {
    font-family: 'Consolas', 'Courier New', monospace;
    font-size: 16px;
  }
</style>
  </style>
  <title>Analysis of Algorithms</title>
</head>
<body>

<div style="display: flex; flex-wrap: wrap;">

  <!-- Box 1 -->
  <div style="flex: 1; width: 100%; background-color: #ECF0F1; padding: 20px; border-radius: 10px; margin: 10px;">

   <p style="font-style: italic;">It is common to estimate the complexity in the asymptotic sense, i.e., to estimate the complexity function for arbitrarily large input. The term <b>"analysis of algorithms"</b> was coined by Donald Knuth.</p>
  </div>

  <!-- Box 2 -->
  <div style="flex: 1; width: 100%; background-color: #D6EAF8; padding: 20px; border-radius: 10px; margin: 10px;">

   <p style="font-style: italic;">Analysis of algorithms is the determination of the amount of time and space resources required to execute it.</p>
  </div>
</div>

<br>

The main concern of analyzing algorithms is the required time or performance. Generally, we perform the following types of analysis:
<br>

<div style="display: flex; flex-wrap: wrap;">

  <!-- Box 1 - Worst-case -->
  <div style="flex: 1; width: 22%; background-color: #F2F3F4; padding: 20px; border-radius: 10px; margin: 10px;">

  <p style="font-style: italic;"><b>Worst-case −</b> The maximum number of steps taken on any instance of size a.</p>
  </div>

  <!-- Box 2 - Best-case -->
  <div style="flex: 1; width: 22%; background-color: #FADBD8; padding: 20px; border-radius: 10px; margin: 10px;">

  <p style="font-style: italic;"><b>Best-case −</b> The minimum number of steps taken on any instance of size a.</p>
  </div>

  <!-- Box 3 - Average case -->
  <div style="flex: 1; width: 22%; background-color: #D5F5E3; padding: 20px; border-radius: 10px; margin: 10px;">

  <p style="font-style: italic;"><b>Average case −</b> An average number of steps taken on any instance of size a.</p>
  </div>

  <!-- Box 4 - Amortised -->
  <div style="flex: 1; width: 22%; background-color: #E8DAEF; padding: 20px; border-radius: 10px; margin: 10px;">

  <p style="font-style: italic;"><b>Amortised −</b> A sequence of operations applied to the input of size averaged over time.</p>
  </div>
</div>

<br>

##### TIME/SPACE COMPLEXITY

<div style="display: flex;">

  <!-- Box 1 - Space Complexity -->
  <div style="flex: 1; width: 48%; background-color: #F0F8FF; padding: 20px; border-radius: 10px; margin: 10px; ">

  <p style="font-style: italic;"><b>“Space complexity”</b> is nothing but the amount of space needed to run to complete the algorithm.</p>
  </div>

  <!-- Box 2 - Time Complexity -->
   <div style="flex: 1; width: 48%; background-color: #D5F5E3; padding: 20px; border-radius: 10px; margin: 10px;">

  <p style="font-style: italic;"><b>“Time complexity”</b> is nothing but the running time needed to run for the completion of the algorithm.</p>
  </div>

</div>

##### Space complexity:-

<div style="background-color: #E6E6FA; padding: 20px; border-radius: 10px; margin: 10px; ">

  <!-- Main Box - Space Complexity -->
  <br>
<p style="font-style: italic;">Amount of space needed by the sum of the two components</p>

  <div style="display: flex;">

 <!-- Sub-Box 1 - Fixed Part -->
<div style="flex: 1; width: 48%; background-color: #F0F8FF; padding: 20px; border-radius: 10px; margin: 10px; ">
      <h4 style="font-size: 18px; font-weight: bold; font-style: italic; text-align: center;">Fixed Part</h4>
      <p style="font-style: italic;">Independent of the characteristics (number and values of inputs and outputs).</p>
      <p style="font-style: italic;">Includes space for the program code, space for simple variables, space for fixed-size components.</p>
    </div>

<!-- Sub-Box 2 - Variable Part -->
<div style="flex: 1; width: 48%; background-color: #D5F5E3; padding: 20px; border-radius: 10px; margin: 10px;">
      <h4 style="font-size: 18px; font-weight: bold; font-style: italic; text-align: center;">Variable Part</h4>
      <p style="font-style: italic;">Consists of space needed by component variables whose size depends on the problem instance.</p>
      <p style="font-style: italic;">Includes space needed by reference variables and the recursion stack.</p>
      <p style="font-style: italic;">S(P) denotes the space required by the program ‘P’.</p>
      <p style="font-style: italic;">S(P) = fixed part + variable part = c + S<sub>P</sub> (instance characteristics)</p>
    </div>

  </div>
</div>

##### Time complexity

<div style="background-color: #E6E6FA; padding: 20px; border-radius: 10px; margin: 10px; ">

<!-- Main Box - Counting Steps -->
<div style="display: flex;">

<!-- Sub-Box 1 - Obtained by Counting -->
<div style="flex: 1; width: 48%; background-color: #F0F8FF; padding: 20px; border-radius: 10px; margin: 10px; ">
   <p style="font-style: italic;">Counting the number of steps in the program.</p>
    </div>

<!-- Sub-Box 2 - Difference from Statements -->
  <div style="flex: 1; width: 48%; background-color: #D5F5E3; padding: 20px; border-radius: 10px; margin: 10px;">
   <p style="font-style: italic;">The step is different from the statement of the program.</p>
    </div>

  </div>
</div>

</body>
</html>








