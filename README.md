# Welcome to the Thrivelife Web Dev Team!

This file will help you onboard into your new position as a web development quality assurance technician. The main responsibility of a QA tech is to ensure high quality work flows between business personnel and our developers. This guide will dig into each pillar of the role, what you can expect, and how to use the tools provided.

# Table of Contents
- [Tools](#tools)
	- [BitBucket](#bitbucket)
	- [Git](#git)
	- [Google_Office](#google_office)
	- [KeePass 2](#keepass_2)
	- [Screencast](#screencast)
	- [Slack](#slack)
	- [SQL_Editor](#sql_editor)
	- [VPN](#vpn)
- [Business Rules](#business_rules)
	- [The_Ws](#the_ws)
  - [Public_Pages](#public_pages)
  - [Delivery_Service](#delivery_service)
  - [Consultant_Tools](#consultant_tools)
  - [Refer_A_Friend](#refer_a_friend)
  - [Recipe_Site](#recipe_site)
- [Tron](#tron)
  - [Sprints](#sprints)
  - [Navigation](#navigation)
	  - [New_Tickets](#new_tickets)
	  - [Browse_Tickets](#browse_tickets)
  - [Taskboard](#taskboard)

# Tools
## BitBucket
## Git
## Google_Office
## KeePass_2
## Screencast
## Slack
## SQL_Editor
## VPN
  
# Business_Rules

Thrivelife is one business of many that we support with manufacturing. As a web dev QA, your sole priority is to support [Thrivelife](https://www.thrivelife.com/). However, you may be asked to support other entities. 

## The_Ws
## Public_Pages
## Delivery_Service
## Consultant_Tools
## Refer_A_Friend
## Recipe_Site

# Tron
## Agile (Scrum Theory)
## Sprints
## Navigation
### New_Tickets
### Browse_Tickets
## Taskboard

# Systems
## Data_Flow
```mermaid
flowchart LR
	subgraph Key
		subgraph Store
		Place1:::stores
		Place1:::stores_key
		end
		subgraph Database
        Place2:::main_key
        Place2:::main
        end
        subgraph Apps
        Place3:::apps_key
        Place3:::apps
        end
        subgraph Endpoint
        Place4:::endpoint_key
        Place4:::endpoint
        end
    end
    subgraph System-Data-Flow
	Peak[\Peak Refuel : Shopify /]:::stores <--> WBIA
	FSN[\FSN : Shopify/]:::stores <--> WBIA
	RUVI[\Ruvi : Shopify/]:::stores <--> WBIA
	TL[\Thrive Live : Magento 2/]:::stores <--> WBIA
	Peak_A[\Peak Refuel : Amazon/]:::stores <--> WBIA
    CSOC[C# OC : Warehouse Manager]:::apps <--> SRWarehouse 
	WBIA[(Web Based Interface App)]:::main <--> CSAI[C# App Integration]:::apps
	CSAI <--> SRWarehouse[(SRWarehouse)]:::main <--> CSAEI[C# App Enlinx Integration]:::apps
    POS([HQ POS : Warehouse Manager]):::endpoint <--> SRWarehouse
    CSAEI <--> Enlinx{Enlix}:::endpoint
    end
classDef default fill:#0000, stroke-width:0px
classDef main stroke-width:1px, fill:#ffff, color:#000, stroke:#000
classDef stores fill:#1da8bd, stroke-width:1px, color:#000, stroke:#000
classDef apps fill:#f8951d, stroke-width:1px, color:#000, stroke:#000
classDef endpoint fill:#7ac143, stroke-width:1px, color:#000, stroke:#000
classDef stores_key color:#1da8bd fill:#1da8bd
classDef main_key color:#ffff
classDef apps_key color:#f8951d
classDef endpoint_key color:#7ac143
```
