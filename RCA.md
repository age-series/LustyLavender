# Modding RCA's

This is a list of things that we have found while running the Lusty Lavender Minecraft Server

## Table of Contents

* AE2
* Bibliocraft
* Buildcraft
* Computronics
* EnderIO
* Forestry
* Journeymap
* Logistic Pipes
* Malisis Doors
* Minechem
* Minefactory Reloaded
* OpenBlocks
* OpenComputers
* Optifine
* Railcraft
* Thaumcraft
* Traincraft

## AE2

* Over time, can cause TPS problems

## BiblioCraft

* Textures can lag slower systems with poor graphics devices

## Buildcraft

* Pipes are inefficient as can be
* Memory leaks in the map implementation due to messy directly allocated byte buffers
  * This causes issues in Logistics Pipes
* Quarries and the filler make the landscape look terrible compared to other miners

## Chisel

* Particle effects on many blocks are very unsightly. Can raise tick timer in config to high value to mitigate somewhat.

## Computronics

* Need to make sure people don't store copyrighted music in the tape drives/speakers/whatever, delete if found, ban applicable players
* Chat boxes can be pretty spammy when players interface with them (eg, "Lights On" "Lights Off" spam from players controlling their base)

## EnderIO

* Over time, EnderIO machines will cause TPS problems

## Forestry

* Beehives everywhere in the world

## Journeymap

* Can't be included in the pack due to license terms

## Logistics Pipes

* Placing pipes in a grid will cause the server TPS to drop
  * Calls into BC code with leaky memory problem (See Buildcraft section)

## Malisis Doors

* Crafting conflict with Eln < 1.16.12 for iron cable

## Minechem

* Rendering is broken and causes ELN devices to have lighting bugs
* Default crafting is difficult
* If you up the crafting requirements, the machines need to be able to hold enough RF for the most expensive craft (otherwise it will never complete)

## Minefactory Reloaded

* Literally spawns sewage, slude, and shit in the world everywhere, looks ugly

## OpenBlocks

* The cartogropher can cause a corrupt chunk that will immediately crash the server/client on load

## OpenComputers

* Compat with Railcraft for routing tracks requires Computronics
* Any calls that are to external components that are not async calls will consume the rest of the OC tick

## Optifine

* Can't be included in the pack due to license terms
* Rendering issue with Chisel blocks (specifically CTM conflicts?)

## Railcraft

* Heat blocks can cause issues
* Unloaded tunnel bores with chunkloaders glitch out sometimes
* Electric tracks load chunks
* Poor ores need to be disabled

## Thaumcraft

* Warp, Taint Biomes
* Portable hole and other block-replacement spells can cause crashes with tile entities
* Nodes everywhere
* Hungry nodes destroy world and can eventually eat large areas if loaded often

## Traincraft

* Sometimes first tier crafting bench freezes client
* All traincars are chunkloaded, including the ones in villages
