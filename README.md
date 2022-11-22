The collection log plugin

Idea: Users should be able to do a command to display their collection log progress

Example usecases
!log {Name}: Barrows (5/24) Icon Icon Icon Icon Icon


Plugins to look at:
Chat Commands, mostly the !pets command
https://github.com/runelite/runelite/tree/master/runelite-client/src/main/java/net/runelite/client/plugins/chatcommands

Collection Log plugin:
https://github.com/evansloan/collection-log

Chat Command:
Multiple Commands that allow the user to display their collection log progress
!clog total: x/1024
!clog Cox: Chambers of Xeric: 2/24 Icon1 Icon2
!clogshort Cox: CoX: 2/24
!clogLong cox: Chamers of Xeric: 2/24 Icon1 Icon2 In X KC

How does the command work?

Lowercase it all.
When we see !clog start:
Grab !clog options such as short, long, total, etc.
Grab !clog name such as Barrows, Misc, CoX, etc.

Search for name and grab data from collection log side.
Replace chat message with Name (completed slots/total slots): Modifiers (icons,etc)

Collection Log:
So this is the tricky part.
We need a way to grab users collection logs.

Most likely: 
User Opens collection log, pull EVERYTHING we can.
Export it to a JSON file that is saved locally for the user.

When Clog command is used, grab that file and search for the name.


Possible Json format of collection log export:
{
  "Collection_Log": {
    "Barrows": {
      "obtained": "22/24",
      "Barrows completions": "1901",
      "items": [
        {
          "Ahrims Hood": "Obtained",
          "count": "3"
        }
      ]
    },
    "Callisto": {
      "obtained": "1/4",
      "Callisto completions": "1901",
      "items": [
        {
          "Callisto Jr": "Obtained",
          "count": "3"
        }
      ]
    },
    "Chambers Of Xeric": {
      "obtained": "22/23",
      "chambers of xeric completions": "1901",
      "items": [
        {
          "Olmlet": "Obtained",
          "count": "3"
        },
        {
          "Dust": "",
          "count": "0"
        },
        {
          "Twisted Bow": "Obtained",
          "count": "1"
        }
      ]
    }
  }
}

Names /w common names:

Abyssal Sire
Sire
Abby Sire

Alchemical Hydra
Hydra
Alch Hydra

Barrows
Barrows Chests
Barrow

Callisto
Calisto
Bear

Cerberus
Cerb

Chaos Elemental
Chaos ele

Chaos Fanatic
Fanatic

Commander Zilyana
Sara
Saradomin
Zily
Zil

Corporeal Beast
Corp

Crazy Archaeologist
Crazy arch
Archaeologist

Dagannoth Kings
Dks
Dag Kings

The Fight Caves
Jad
Fight Caves
Yad

The Gauntlet
Gauntlet
Cg
Corrupted Gauntlet

General graardor
General garage door
Garage door
bandos
Goblin king

Giant Mole
Mole

Grotesque Guardians
GGs

Hespori

The inferno
zuk

Kalphite Queen
KQ

King Black Dragon
KBD

Kraken

Kree'arra
Arma
Kree

K'ril Tsutsaroth
Kril
K'ril
Zammy
Zamorack

Nex

The Nightmare
nightmare
Phsoani (check spelling)

Obor

Sarachnis
Saracha

Scorpia
Scorpian
Scorp

Skotizo
Skotzo

Tempoross
Temp

Thermonuclear Smoke Devil
Thermy

Venenatis
Venatntis
venanatos
Veninatos
Venny
Ven

Vet'ion
Vetion
Vet

Vorkath
Vork
Vorky

Wintertodt
WT
wintertoad
wintertodd

Zalcano
Zalc

Zulrah
Snake
Zulruh

Chambers of xeric
Cox
Xeric
Chambers
Raids 1
Raid 1
olm

Theatre of blood
Tob
theatre
verzik

Tombs of amascut
Tombs
wardens
amascut

Beginner Treasure Trails
Beginner Clues
Beginner
Beginner Clue

Easy Treasure Trails
easy clue
easy clues
easys

Medium Treasure Trails
Medium clues
mediums
Medium clue

Hard Treasure Trails
Hard Clue
Hard clues
Hards

Elite Treasure Trails
Elite
Elite Clues
Elite Clue

Master Treasure Trails
Master clues
master clue
master

Shared Treasure Trail Rewards
Shared clues
All Clues

Hard Treasure Trail Rewards (Rare)
Hard Rares
Hard Clue Rares
Hard Treasure Trail
Hard Treasure Trail Rewards

Elite Treasure Trail Rewards (Rare)
Elite Rares
Elite Clue Rares
Elite Treasure Trail
Elite Treasure Trail Rewards

Master Treasure Trail Rewards (Rare)
Master Rares
Master Clue Rares
Master Treasure Trail
Master Treasure Trail Rewards

Barbarian Assault
Barb assult
Barb assault
BA

Brimhaven Agility Arena
Brimhaven agility
Brimhaven
Brim agility
Brim

Castle Wars
CW
Castle war

Fishing Trawler
Fishing trawlers

Giants' Foundry
Giants foundry
giant's foundry
GF

Gnome Restaurant

Guardians of the rift
gotr
guardians

Hallowed Sepulchre
Hallowed
Hallowed Sep
Sep

Last man standing
LMS

Magic training Arena
MTA

Mahogany Homes
Mahog Homes

Pest Control
PC

Rogues' Den
Rogues den
Rogue's den
rouge's den
rouges den

Shades of mort'ton
Shades of morton
shadoes of mortton

Soul wars

Temple Trekking

Tithe Farm
Tithe
Tit farm

Trouble Brewing

Volcanic Mine
VM

Aerial Fishing
arial fishing

All pets

Camdozaal
Camdozal

Champion's Challenge
Champions challenge
champions' chllenge

Chaos druids
Chaos druid

Chompy birds
Chompys
Chompy

Creature Creation
Creatures

Cyclopes
Cyclope

Fossil island notes
fossil island

Glough's experiments
Demonics
Demonic Gorrillas 
Gloughs experiments

Monkey backpacks
ape atoll agility

motherload mine
motherlode mine

my notes
my note

Random events
Randoms

Revenants
Revs

Rooftop agility
Rooftops

Shayzien Armour
Shayzien

Shooting stars
stars

skilling pets
skill pets

slayer

tzhaar

miscellaneous
misc
miscellaneus
miscs


