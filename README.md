# FoEInvestmentAdvisor
<i>Optimal FP distribution among provided GBs for maximum guaranteed profit </i>


<h2>Requirements specification:</h>
<br>
<h3>General directions</h3>
<ul>
  <li>Desktop application that works on windows XP and above</li>
  <li>Aims to provide an easy-to-use, smooth interface</li>
  <li>After the necessary information input the software should give the user clear advice on how to optimally distribute forge points among the provided GBs for maximum guaranteed profit</li>
</ul>
<br>
<h3>UI</h3>
<ul>
  <li>Since there might be other tools included in the app later on, the first window seen by the user after opening the app should be a tool-selection menu, with one option, initially: "Investment advisor"</li>
  <li>The window that pops up after selecting the Investment advisor tool should first ask for the Arc level of the player and the amount of FPs he has available for distribution (same design as the GB level selector described below), and then -after these are submitted- display the input form, where the user can enter the GB data the program will work with. One form refers to one GB at a time, and should include: 
    <ul>
      <li>A textboxt to enter the name of the player who owns the GB in question.</li>
      <li>A dropdown list where the name of the GB can be selected. While this box is in focus, if the user starts typing the first list-element with a name that contains the typed text should be selected (this should be triggered after each entered letter). Arrow keys should be usable as well for navigating the drop-down list. Pressing tab while in a drop down list should result in selecting the current list-element chosen and jumping to the next form input-box.</li>
      <li>A dropdown list where the current level of the GB can be selected. Upon selecting the level, the program should automatically display the total amount of FPs needed for the next level of that GB and the rewards for each contributor position. Arrow keys should be usable for navigating the drop-down list, as well as typing the number (e.g. pressing 1 and then 5 should first result in choosing the 1st element, then the 15th). Pressing tab while in a drop down list should result in selecting the current list-element chosen and jumping to the next input-box of the form.</li>
      <li>Five fields where the FPs already contributed by other players or the user can be entered for each position. Upon entering these numbers the program should automatically add the points to a "Total amount of FPs already contributed" bar displayed on the form and calculate the displayed value for the "Further points needed for levelup" bar. There should be a button for adding additional contributor positions to the default five. Each contributor-position-field should have a boolean slider that the user can set to 1 if they are the ones who currently occupy that position, and 0 if it's another player. The sum of the values of all these boolean sliders of a form has to be one or zero, so upon changing a slider from zero to one, the rest of the sliders should automatically be set to zero.</li>
      <li>Arrow buttons for navigating back and forth between GBs already entered</li>
      <li>An add another GB button</li>
      <li>A calculate optimal FP distribution button. Pressing this means the user is done adding GBs and the program can start the calculations.</li>
      <li>A "Delete" button that discards the currently edited GB and jumps back to the last submitted GB. If the one and only GB form is being edited, pressing this button should direct the user back to the tool-selection menu. User should be warned and asked for confirmation.</li>
      <li> A "Discard all" button that allows the user to navigate back to the results screen if they have already submitted the forms once, otherwise it should navigate back to the main tool-selection menu. This should result in losing all changes made since the last submittion in case they have already submitted once, otherwise just discarding all the data. User should be warned and asked for confirmation.</li>
      <p><i>
        Hotkeys:
        <ul>
          <li>TAB -> Next logical form element</li>
          <li>NUM+ -> Add another GB</li>
          <li>DEL -> Delete current GB form</li>
          <li>ENTER -> If a form element is in focus, confirm current input and jump to next form input element or in case of the last input element it should trigger the calculate optimal FP distribution button, if no elements are selected it should also trigger the calculate optimal FP distribution button, if a button is in focus, it should just trigger that.</li>
        </ul>
      </i></p>
    </ul>  
  </li>
  <li>Upon pressing the "Calculate optimal FP distribution" button, -after a brief but cool loading animation- the results are to be displayed on a grid. Each grid element consists of a player-name, an advised FP investment amount, and the expected rewards. The player-name should be coloured red, yellow or green based on how the invested amount compares to the earned amount. There is to be a message templates button that offers an appropriate text as a reaction for each colour. Red means the user will earn so much FP that an apology is in order, green means the user barely won anything, or didnt get any FPs, just other rewards (in this case the suggested message would be along the lines of: "sorry to contribute without asking first, I hope it's okay").  Upon selecting a grid element the user should be navigated to a GB-form identical to the one he submitted, where the input data can be edited once again. The Discard all button and the Add another GB button should be available here (on the result screen) as well. Upon hovering a grid element, a small X should appear at the upper right corner of it, which should allow the deletion of the GB data, similarly to the Delete button of a GB form. The total amount of FPs spent and all the rewards should also be displayed neatly on this screen.</li>
</ul>
