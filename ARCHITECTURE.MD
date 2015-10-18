# Architecture

## Overview
The idea is to separate PHPTeamUp into few smaller applications, which can talk to each other via APIs.
That way, development process would be easier to manage (there can be different teams, each working on one of the parts).
Also, separated architecture is more flexible. We could use each sub-app in many ways, maximising usefullness of PHPTeamUp in general.

For now, we're thinking about three apps - Domain, Contacts, and Frontend.

## PHPTeamUp Domain
This would be the heart of the project, holding all the domain logic, responsible for managing user interaction.

## PHPTeamUp Contacts
Reposible for holding user data and managing authentication. We're thinking about private and public layers. Private for 
PHPTeamUp usage only (with all the sensitive stuff), and public for authentication (may be used by anyone).

## PHPTeamUp Frontend
Face of the application. Responsible for everything that happens on the client's side.
