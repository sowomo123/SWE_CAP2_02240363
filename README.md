# Programming the Farming Drone(Report)

# Introduction
 Briefly describe the game and the objective?
 This is a programming game which induce a various agriculture task 
 there are various code 
 # bojective
 the objective of playing the programming game is to learn and improve programming skills in an engaging, interactive way. Programming games turn coding into a game-based experience, helping players develop problem-solving abilities, understand logic structures, and become more comfortable with syntax and algorithms. 
 
 # TableofContents
  -[CodeSnippetsandExplanation](#code-snippets-and-explanation)-
   [Challenges andLearnings](#challenges-and-learnings)- [References](#references)

# Code-Snippets-and-Explanation

# step1
while true:
  if can_harvest():
    harvest()

# explanation 
The code runs an infinite number of times and harvest the grass with the if condition

# video
<video controls src="step1.mp4" title="step 1 "></video>

# notes
- Using the code above I was able to get enough hay to unlock the tile
- These features were unlocked too: variables and functions.

# step2: farming on 3*3 tiles 
while True:
  if can_harvest():
  harvest()
  move(north)

  # explanation
this code makes it harvest from south to north in 3*3 tiles 

# video
<video controls src="step2.mp4" title="step2"></video>

# notes
it is much more efficient and has speed up a bit and it harvest hay

# step 3 harvest wood
while True:
  plant(entities.Bush)
  if can_harvest():
   harvest()
   move(north)
 else move (north)
 # explanation
 this code will harvest wood
 # video
 <video controls src="step3.mp4" title="step3"></video>
 # notes
 it will harvest wood with more efficient way

# step4
clear()
move (south)
while true:
  for i in range(get_world_size_()):
    move north()
    if can_harvest():
       harvest()
    if num_items(item.hay)< 500:
       plant(entities.grass)
    elif num_items(items.wood) < 100:
        plant (entities.bush)
    else:
    if num_ items(Items.carrots_seed) == 0:
      trade(Items.carrot_seed)
    if get_ground_type() == grounds.turfs:
       till
     plant(entities.carrots)
     move(east)
# explanation
this code will harvest bush and grass, it will trade carrot seed and it will harvest carrot seed 
# video
<video controls src="step4.mp4" title="step4"></video>
# notes
turfs is a dictionary where each key represents a turf’s location and each value represent like (bush,hay,trees,carrots seeds,etc)
get_ground_types:This function will take the coordinates of the center turf and a range as arguments, and return a list of unique ground types within that range.

# step5
clear()
move (south)
while true:
  for i in range(get_world_size_()):
    move north()
    if can_harvest():
       harvest() 
# trade water tank
       if num_items(item.water_tank) < 100:
       trade(item.Empty_tank)
    if num_items(item.hay)< 500:
       plant(entities.grass)
    elif num_items(items.wood) < 100:
        plant (entities.bush)
    else:
    if num_ items(Items.carrots_seed) == 0:
      trade(Items.carrot_seed)
    if get_ground_type() == grounds.turfs:
       till
     plant(entities.carrots)
     move(east)
# explanation
this code with trade empty tank with woods
the more empty 
# video
  <video controls src="step5.mp4" title="step5"></video>

# notes
by exchanging the watertank it will give water to the plants and will increse the growth

# step6
while True:
	move(North)
	plant(Entities.Tree)
	if can_harvest():
		harvest()
	plant(Entities.Tree)
	if can_harvest():
		harvest()
	move(North)
	plant(Entities.Tree)
	if can_harvest():
		harvest()
	plant(Entities.Tree)
	if can_harvest():
		harvest()
	move(West)
	plant(Entities.Tree)
	if can_harvest():
		harvest()
	plant(Entities.Tree)
	if can_harvest():
		harvest()
	
# explanation
this code helps to plant the trees and harvrst wood
# video
<video controls src="step6.mp4" title="step 6"></video>

# notes
by planting the trees we will be able to harvest the trees

# step7
while True:
	for x in range(get_world_size()):
		move(East)
		trade(Items.Sunflower_Seed, 100)
		for y in range(get_world_size()):
				if can_harvest():
					harvest()
				till()
				plant(Entities.Sunflower)
				move(South)
# expalnation
this code will help us to grow sunflower as well as hay
 # video
 <video controls src="step7.mp4" title="step7"></video>

 # notes
by growing this sun flower we will be able to get the power

# step 8
def watering():
   if num_items(Items.Water_Tank):
	trade(Items.Empty_Tank)
	
	if get_water() < 0.8:
		use_item(Items.Water_Tank)
# explanation
this code will help to water the plant
# video
<video controls src="step 8.mp4" title="step8"></video>

# notes
it will increase the growth of plant

# step 9
def planting():
	if num_items(Items.Hay) < HayCap:
		if get_ground_type() == Grounds.Turf:
			till()
		plant(Entities.Grass)
		#woods
	elif num_items(Items.Wood) < WoodCap:
		if get_ground_type() == Grounds.Turf:
			till()
		plant(Entities.Bush)
		#carrots
	elif num_items(Items.Carrot) < CarrotCap:
		if get_ground_type() == Grounds.Turf:
			till()
		plant(Entities.Carrots)
# pumkin
	elif num_items(Items.Pumpkin) < PumkinCap:
		if num_items(Items.Pumpkin_Seed) == 0:
			trade (Items.Pumpkin_Seed, 5)
		if get_ground_type() == Grounds.Turf:
			till()
		plant(Entities.Pumpkin)

# explanation
this code will harvest the not only pumkin but also other harvest such as hay woods and carrots
# video
<video controls src="step 9.mp4" title="step 9"></video>

# notes
we used count_ground_types that operates on a collection of items (in this case, "turfs"), num_items typically refers to the total number of items (turfs) that meet certain criteria within a specified area or range.

# step 10
def BuyStuff():
	if num_items(Items.Fertilizer) < 2000:
		trade(Items.Fertilizer, get_world_size())

# explanation
this code will help to get fertalizer for the crops
# video
<video controls src="step 10.mp4" title="step 10"></video>

# step 11
move(south)
# explanation
this will help to reset the position of the drone
# video
<video controls src="step 11.1.mp4" title="Title"></video>

# notes
this help went harvest are not in order