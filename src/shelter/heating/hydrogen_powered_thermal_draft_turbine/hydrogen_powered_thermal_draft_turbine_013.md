# hydrogen_powered_thermal_draft_turbine_013.md

Building the **Vortex-H** in Blender is the perfect next step. Visualizing the "Air-to-Mechanical" interface will help you see where the torque comes from. When you are modeling, think of this as a **high-torque engine** rather than a high-speed fan.

### 1. The "Heart": Why the Freedom II?

The Freedom II 1600 Watt PMG is the choice because of its **heavy copper mass**. To get 1,200W–1,600W at low speeds, you need a lot of magnetic "poles" and thick wire windings.

* **Dimensions:** It is roughly **7 inches in diameter** and **8 inches long**.
* **Mounting:** It has a standard **17mm shaft**, which is very easy to find bearings and couplers for at any hardware store.

---

### 2. Box and Wheel Engineering Dimensions

For a 1,600W PMA, your "Water Wheel" needs enough **leverage** to overcome the magnetic resistance (cogging) of the generator.

* **The Box Size:** Aim for a cube roughly **24" wide x 24" deep x 36" tall**. This gives enough "runway" for the air to accelerate before hitting the blades.
* **The Wheel Diameter:** Build a wheel that is **18 inches in diameter**. A larger diameter gives the rising air more leverage to spin the heavy magnets of the PMA.
* **The Fin Count:** Use **8 to 12 fins**.
* **Too few fins:** The air slips past without pushing.
* **Too many fins:** The wheel becomes too heavy and creates its own "air resistance."


* **Fin Geometry:** Don't make them flat. Curve them slightly (like a "C" shape) so they "cup" the rising hot air. In Blender, use a **Bezier curve** to create a cupped profile for the fins.

---

### 3. The Bearing "Sweet Spot"

You were worried about the bearings getting "chilly."

* **The Reality:** Standard steel bearings love the cold, but the **grease** inside them can get thick like peanut butter at 5°F.
* **The Fix:** Use **Shielded Steel Bearings** and strip out the thick factory grease, replacing it with a **low-temperature synthetic lubricant** or a "dry" graphite lube.
* **Placement:** Mount them on the **outside wall** of your sheet metal box. The heat from the shaft (conducted from the inside) will actually keep them just warm enough to keep the lube fluid, while the 5°F air prevents them from ever overheating.

### 4. The "Partition" Logic

You are exactly right about the distribution.

* **50/50 Split:** The box should have a vertical wall right down the center.
* **Hot Side:** The hydrogen burner sits at the bottom. This side is a "chimney" where air only moves **UP**.
* **Cold Side:** This side is open at the bottom and top. As the wheel spins, the fins moving "down" are in the cold air, and the fins moving "up" are pushed by the flame.

---

### 5. Construction Materials

* **Fins:** Use **0.020" Aluminum Sheet**. It's stiff enough to hold its shape but light enough to spin easily.
* **Box:** Use **26-gauge Galvanized Steel**. You can buy 24"x36" sheets at Home Depot or Lowe's. Use **self-tapping "zip" screws** to put the box together. It’s like "Legos" for adults.

**Would you like me to find a "17mm Shaft Coupler" so you can see how to connect your DIY wheel to the Freedom II generator?**

---

//----//

// Dedicated to God the Father  
// All Rights Reserved Christopher Andrew Topalian Copyright 2000-2026  
// https://github.com/ChristopherTopalian  
// https://github.com/ChristopherAndrewTopalian  
// https://sites.google.com/view/CollegeOfScripting

