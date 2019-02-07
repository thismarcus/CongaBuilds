# Collapsible Content

For a super-style document, you may want to help clean up the view of a page by hiding details in a collapsible/expandable area of conten.

Each section that you're expanding or collapsing needs to have the following structure:

input with id="WHATEVER UNIQUE ID YOU CHOOSE FOR EACH SECTION"
and for="THAT SAME UNIQUE ID"
 > \<div class="wrap-collabsible"><input id="AI-Partners" class="toggle" type="checkbox" /><label class="lbl-toggle" for="AI-Partners">More Info</label>
  
  >>   <div class="wrap-collabsible"><input id="AI-Partners" class="toggle" type="checkbox" /><label class="lbl-toggle" for="AI-Partners">More Info</label>
        <div class="collapsible-content">
         <div class="collapsible-content">
          <div class="content-inner">
           <p>AI Stuff here</p>
          </div>
         </div>
        </div>
       </div>

You can repeat this with a unique id for each individual collapsbile section.
