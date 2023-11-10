<h3>Clothing</h3> 
<input type="checkbox" id="thermalUnderwear" name="clothing1">&nbsp;<label for="thermalUnderwear">**Thermal Underwear**: Essential for layering.</label><br>
<input type="checkbox" id="warmSweaters" name="clothing2">&nbsp;<label for="warmSweaters">**Warm Sweaters/Fleece**: Wool or synthetic.</label><br>
<input type="checkbox" id="waterproofJacket" name="clothing3">&nbsp;<label for="waterproofJacket">**Waterproof and Windproof Jacket**: A must in unpredictable weather.</label><br>
<input type="checkbox" id="waterproofPants" name="clothing4">&nbsp;<label for="waterproofPants">**Waterproof Pants**: Ideal for rainy days or waterfalls.</label><br>
<input type="checkbox" id="hikingBoots" name="clothing5">&nbsp;<label for="hikingBoots">**Hiking Boots**: Waterproof and comfortable for walking.</label><br>
<input type="checkbox" id="casualShoes" name="clothing6">&nbsp;<label for="casualShoes">**Casual Shoes**: For city exploration in Reykjavik.</label><br>
<input type="checkbox" id="warmSocks" name="clothing7">&nbsp;<label for="warmSocks">**Warm Socks**: Preferably woolen.</label><br>
<input type="checkbox" id="accessories" name="clothing8">&nbsp;<label for="accessories">**Gloves, Scarf, and Beanie**: For extra warmth.</label><br>
<input type="checkbox" id="swimwear" name="clothing9">&nbsp;<label for="swimwear">**Swimwear**: For hot springs or pools.</label><br>
<input type="checkbox" id="comfortableTrousers" name="clothing10">&nbsp;<label for="comfortableTrousers">**Comfortable Trousers/Jeans**: For casual outings.</label><br>
<input type="checkbox" id="shirts" name="clothing11">&nbsp;<label for="shirts">**T-Shirts and Long-Sleeve Shirts**: For layering.</label><br>

<h3>Electronics</h3> 
<input type="checkbox" id="camera" name="electronics1">&nbsp;<label for="camera">**Camera and Charger**: To capture the scenic beauty.</label><br>
<input type="checkbox" id="mobilePhone" name="electronics2">&nbsp;<label for="mobilePhone">**Mobile Phone and Charger**: For communication and navigation.</label><br>
<input type="checkbox" id="adapter" name="electronics3">&nbsp;<label for="adapter">**Universal Travel Adapter**: Iceland uses European plug type C.</label><br>
<input type="checkbox" id="powerBank" name="electronics4">&nbsp;<label for="powerBank">**Power Bank**: To keep your devices charged on the go.</label><br>

<h3>Travel Essentials</h3>
<input type="checkbox" id="backpack" name="travel1">&nbsp;<label for="backpack">**Backpack**: For day trips and hiking.</label><br><input type="checkbox" id="sunglasses" name="travel2">&nbsp;<label for="sunglasses">**Sunglasses and Sunscreen**: Protection against UV rays.</label><br>
<input type="checkbox" id="waterBottle" name="travel3">&nbsp;<label for="waterBottle">**Water Bottle**: Stay hydrated.</label><br>
<input type="checkbox" id="maps" name="travel4">&nbsp;<label for="maps">**Maps and Guidebooks**: For navigation and information.</label><br>
<input type="checkbox" id="insurance" name="travel5">&nbsp;<label for="insurance">**Travel Insurance Documents**: Always carry a copy.</label><br>
<input type="checkbox" id="passport" name="travel6">&nbsp;<label for="passport">**Passport and ID**: Essential for international travel.</label><br>

<h3>Toiletries and Health</h3>
<input type="checkbox" id="toiletriesKit" name="health1">&nbsp;<label for="toiletriesKit">**Basic Toiletries Kit**: Toothbrush, toothpaste, shampoo, etc.</label><br>
<input type="checkbox" id="lipBalm" name="health2">&nbsp;<label for="lipBalm">**Lip Balm and Moisturizer**: To combat dry weather.</label><br>
<input type="checkbox" id="firstAid" name="health3">&nbsp;<label for="firstAid">**First Aid Kit**: Including personal medications.</label><br>
<input type="checkbox" id="sanitizer" name="health4">&nbsp;<label for="sanitizer">**Hand Sanitizer and Face Masks**: For hygiene and safety.</label><br>

<h3>Miscellaneous</h3>
<input type="checkbox" id="snacks" name="misc1">&nbsp;<label for="snacks">**Snacks**: For long drives or hikes.</label><br>
<input type="checkbox" id="reusableBag" name="misc2">&nbsp;<label for="reusableBag">**Reusable Bag**: For shopping or carrying extra items.</label><br>
<input type="checkbox" id="notebook" name="misc3">&nbsp;<label for="notebook">**Notebook and Pen**: To jot down experiences or directions.</label><br>
<input type="checkbox" id="binoculars" name="misc4">&nbsp;<label for="binoculars">**Binoculars**: For wildlife watching or scenic views.</label><br>

<h3>For Specific Activities</h3>
<input type="checkbox" id="hikingGear" name="activities1">&nbsp;<label for="hikingGear">**Hiking Gear**: If planning extensive hiking.</label><br><input type="checkbox" id="photoAccessories" name="activities2">&nbsp;<label for="photoAccessories">**Photography Accessories**: Like tripods for Northern Lights photography.</label><br>
<input type="checkbox" id="waterproofCase" name="activities3">&nbsp;<label for="waterproofCase">**Waterproof Case for Electronics**: In case of wet conditions.</label><br>

<script>
  // JavaScript to handle persistence
  const checkboxes = document.querySelectorAll('input[type="checkbox"]');

  checkboxes.forEach((checkbox) => {
    // Load the checkbox state from localStorage (if available)
    const checkboxId = checkbox.id;
    if (localStorage.getItem(checkboxId) === 'checked') {
      checkbox.checked = true;
    }

    // Add an event listener to save the checkbox state when it changes
    checkbox.addEventListener('change', () => {
      if (checkbox.checked) {
        localStorage.setItem(checkboxId, 'checked');
      } else {
        localStorage.removeItem(checkboxId);
      }
    });
  });
</script>
