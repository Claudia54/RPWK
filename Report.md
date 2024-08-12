# Elden of the Rings

## Introduction
In the context of the course on Web Knowledge Representation and Processing, we created an ontology based on the game "Elden Ring". For this purpose, datasets found on the Kaggle platform were used. The datasets included files for the following data: sorceries, items, bosses, incantations, locations, spirits, talismans, shields, creatures, classes, ashes, armors, ammos, NPCs, and weapons.

## Explanation of the datasets
As previously mentioned, this dataset was divided into the following files:

sorceries,
items,
bosses,
incantations,
locations,
spirits,
talismans,
shields,
creatures,
classes,
ashes,
armors,
ammos,
NPCs,
weapons.
These will compose the majority of the classes created in the ontology (which will be explained later). The datasets available on Kaggle had some samples with missing or incorrect information, such as "crystal tears" instead of "crystal tear," as well as certain entries where the damage and defense values of objects were incomplete or poorly formatted. Therefore, a careful analysis of all datasets was necessary to complete the samples by examining the original game or deleting rows where the information was not available on the official "Elden Ring" website.

The columns of the different datasets were also analyzed, and some that were not considered important for our ontology were deleted. For example, the "types" column in the incantations dataset contained only words like "Incantation" or "Incantations."

## Ontology
In creating the ontology, various classes, subclasses, data properties, and object properties were defined. This ontology aims to answer questions such as:

"What items are available in the game?"
"Which region does each location belong to?"
"Which bosses can be found in each region?"
"Where can certain creatures be found?"
"What items are received after defeating a boss?"
"What items are found after defeating a boss?"
The ontology will be used by game developers, researchers in game studies, and enthusiasts who wish to deepen their knowledge about "Elden Ring".

### Classes and Subclasses
The classes represent broad categories of entities, while the subclasses are more specific groupings within these categories. In the "Elden Ring" ontology, we have several classes, such as Ammos, which represents types of ammunition used in the game; Armors, which covers all types of protective equipment; Ashes, which refers to items related to the summoning of spirits; Bosses, which includes all the major adversaries that players encounter; and Classes, which are the different character classes that players can choose from. Within Classes, we have subclasses such as Astrologer, Bandit, Confessor, Hero, Prisoner, Prophet, Samurai, Vagabond, Warrior, and Wretch.

Other classes include Creatures, which encompasses various enemies; Incantations, which represents spells and magical abilities; Items, a general category for all usable items in the game, with subclasses such as Consumable, items that can be used once; Crystal_Tear, items used for specific buffs or abilities; Info_Item, items that provide information; Key_Item, important items necessary for game progression; Misc, various miscellaneous items; and Reusable, items that can be used multiple times. There are also Npcs, non-playable characters in the game; Region, geographic areas within the game world; Shields, defensive equipment with subclasses such as Greatshield, Medium_Shield, and Small_Shield. Additionally, we have Sorceries, specific types of magical spells; Spirits, summonable entities that assist the player; Talismans, items that grant passive bonuses; and Weapons, offensive equipment with numerous subclasses, including Axe, Ballista, Bow, Claw, Colossal_Sword, Colossal_Weapon, Crossbow, Curved_Greatsword, Curved_Sword, Dagger, Fist, Flail, Glintstone_Staff, Greataxe, Greatbow, and others.

### Object Properties
The object properties define the relationships between different entities. The `bossDrops` property specifies the items that bosses drop when defeated, with its domain in Bosses and its range including Armors, Ashes, Incantations, Items, Shields, Sorceries, Spirits, Talismans, and Weapons. The `creatureDropsItem` property specifies items dropped by creatures, with its domain in Creatures and its range in Items. The `isInLocation` property indicates the location of bosses, creatures, and NPCs, with its domain including Bosses, Creatures, and Npcs, and its range in Location. The `isInRegion` property specifies the region of bosses, creatures, locations, and NPCs, with its domain including Bosses, Creatures, Location, and Npcs, and its range in Region.

### Data Properties
The data properties define the attributes and characteristics of entities. The `affinity` property applies to Ashes, defining their elemental or magical alignment. The `damageNegation` property is used for Armors, indicating how much damage they can negate. The `damageType` property describes the type of damage for Ammos, Shields, and Weapons. The `defenceType` property specifies the type of defense for Armors, Shields, and Weapons. The `description` property provides a textual description for all entities in our ontology, facilitating the transmission of information that other data might not provide. The `effect` property describes the effects of Incantations, Items, Sorceries, Spirits, and Talismans. The `fpCost` property indicates the focus points cost for Incantations, Sorceries, and Spirits, which may or may not exist (only in the case of Spirits). The `healthPoints` property applies to Bosses, specifying their health points. The `hpCost` property specifies the health points cost for Spirits, which may or may not exist. The `image` property links to an image for various entities, including Ammos, Armors, Ashes, Bosses, Classes, Creatures, Incantations, Items, Npcs, Region, Shields, Sorceries, Spirits, Talismans, and Weapons. The `passive` property describes the passive effects for Ammos. The `quote` property contains quotes for Npcs. The `requiresAttributes` property specifies the attributes required for Incantations, Shields, Sorceries, and Weapons. The `resistance` property indicates resistance values for Armors. The `role` property defines the role of Npcs. The `scalesWith` property indicates which attributes weapons or shields scale with for Shields and Weapons. The `skill` property describes the skills associated with Ashes. The `slots` property indicates the number of slots used by Incantations and Sorceries. The `weight` property specifies the weight of Armors, Shields, and Weapons.

## Application Development
The developed application is an interactive web platform that allows users to explore detailed data from the game Elden Ring. Using a user-friendly interface, the application enables navigation through various categories of information, such as weapons, items, locations, regions, NPCs, and more. Each category is presented in organized lists, and by clicking on a specific item, the user is directed to a detailed page containing enriched information, including images and detailed descriptions.

#### Features
- **Home Page**: The home page offers links to all main categories, allowing easy navigation.
- **Item Exploration**: Items are categorized by subclasses. Each subclass lists all corresponding items with their respective names and images.
- **Item Details**: By clicking on an item, the user can see a detailed description of the item, its effects, requirements, and, if applicable, the boss that needs to be defeated to obtain it.
- **Region Exploration**: The regions of the game are listed, and by selecting a region, the user can see all locations and bosses present in that region.
- **Location Details**: Include descriptions, images, and links to related regions.
- **NPC Exploration**: List of NPCs with images and detailed descriptions of their role in the game and their location.
- **Weapon Exploration**: Weapons are categorized by types. Each type lists all corresponding weapons with their respective names and images.
- **Weapon Details**: By clicking on a weapon, the user can see a detailed description of the weapon, its requirements, statistics, and, if applicable, the boss that needs to be defeated to obtain it.
- **Shield Exploration**: Shields are categorized by types. Each type lists all corresponding shields with their respective names and images.
- **Shield Details**: By clicking on a shield, the user can see a detailed description of the shield, its requirements, statistics, and, if applicable, the boss that needs to be defeated to obtain it.
- **Incantation Exploration**: The incantations of the game are listed, and by selecting an incantation, the user can see a detailed description of the incantation, its requirements, statistics, and, if applicable, the boss that needs to be defeated to obtain it.
- **Spell Exploration**: The spells of the game are listed, and by selecting a spell, the user can see a detailed description of the spell, its requirements, statistics, and, if applicable, the boss that needs to be defeated to obtain it.
- **Armor Exploration**: Armors are categorized by types. Each type lists all corresponding armors with their respective names and images.
- **Armor Details**: By clicking on an armor, the user can see a detailed description of the armor, its statistics, and, if applicable, the boss that needs to be defeated to obtain it.
- **Ashes Exploration**: The ashes of the game are listed, and by selecting an ash, the user can see a detailed description of the ash, the skill associated with it, its affinity, and, if applicable, the boss that needs to be defeated to obtain it.
- **Talisman Exploration**: The talismans of the game are listed, and by selecting a talisman, the user can see a detailed description of the talisman, its effects, and, if applicable, the boss that needs to be defeated to obtain it.
- **Spirit Exploration**: The spirits of the game are listed, and by selecting a spirit, the user can see a detailed description of the spirit, its requirements (health points, focus points, or none), its effect, and, if applicable, the boss that needs to be defeated to obtain it.
- **Class Exploration**: The classes of the game are listed, and by selecting a class, the user can see a detailed description of the class, its attributes, starting weapon, shield, and armors.
- **Ammo Exploration**: The ammunitions of the game are listed, and by selecting an ammo, the user can see a detailed description of the ammo, its attributes, and passive effects, if any.
- **Adding New Entries to the Ontology**: Through a button on the home page, users can select the type of new entity to add. The options include the previously enumerated classes, Items, Region, Location, NPC, Weapon, Shield, Armor, Talisman, Ashes, Spirits, Classes, Bosses, and Ammos. After selecting the type, the user is directed to a page that contains the necessary and optional fields that must be filled out to correctly add that element to the ontology.
- **Removing an Entry from the Ontology**: It is possible on each entry's page to remove it from the ontology through a button. After pressing this button, the entry is removed, and the user is redirected to the page of the type of element just removed.

#### Development
The application was developed using the Flask framework for creating web applications in Python. Flask was configured to define routes that respond to different URLs, facilitating navigation between different sections of the application. For data persistence and retrieval, GraphDB, an RDF database, was used, allowing SPARQL queries for semantic data manipulation. SPARQL queries were written to extract RDF data from GraphDB, and these queries were integrated into Flask routes to fetch dynamic information according to the user's needs.

For rendering web pages, Jinja2 templates were used. These templates allow dynamic data insertion into HTML. The interface was created using CSS, with the W3.CSS framework, ensuring a clean and responsive design.

## Conclusion
The application offers a robust platform for exploring detailed information about the game Elden Ring, using modern web development technologies and semantic databases. The modular structure of the code facilitates future expansions and maintenance, ensuring that the application remains useful and relevant as new data, links, or functionalities are added.
