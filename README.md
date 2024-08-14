# German Bundesliga API Documentation

This documentation provides details on the various endpoints available in the German Bundesliga API. The API provides data related to games, teams, players, and other relevant information about the Bundesliga.

This API is listed on RapidAPI -> [https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/german-bundesliga-api](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/german-bundesliga-api)

## Table of Contents
1. [BoxScore](#boxscore)
2. [Game Summary](#game-summary)
3. [Schedule](#schedule)
4. [Scoreboard](#scoreboard)
5. [Standings](#standings)
6. [Team List](#team-list)
7. [Team Info](#team-info)
8. [Team Roster](#team-roster)
9. [News](#news)
10. [Player Season](#player-season)
11. [Player Leagues](#player-leagues)
12. [Player Statistics](#player-statistics)
13. [Team Statistics Discipline](#team-statistics-discipline)
14. [Team Statistics Scoring](#team-statistics-scoring)
15. [Team Performance](#team-performance)
16. [Team Transfers](#team-transfers)
17. [Tables](#tables)
18. [Injuries](#injuries)
19. [Team Results](#team-results)
20. [Player Overview](#player-overview)
21. [Player Statistics](#player-statistics-1)
22. [Player Bio](#player-bio)
---

## BoxScore

Get the box score for a specific game.

**Endpoint:** `/boxscore`

**Method:** GET

**Query Parameters:**
- `gameId` (required): The ID of the game

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if gameId is missing
- Error: 500 Internal Server Error if an error occurs

---

## Game Summary

Get the summary for a specific game.

**Endpoint:** `/summary`

**Method:** GET

**Query Parameters:**
- `gameId` (required): The ID of the game

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if gameId is missing
- Error: 500 Internal Server Error if an error occurs

---

## Schedule

Get the schedule for a specific date.

**Endpoint:** `/schedule`

**Method:** GET

**Query Parameters:**
- `year` (required): The year
- `month` (optional): The month (default: 01)
- `day` (optional): The day (default: 01)

**Note:** If the link doesn't contain the base URL, remember that the base URL is https://espn.com

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if year is missing
- Error: 500 Internal Server Error if an error occurs

---

## Scoreboard

Get the scoreboard for a specific date.

**Endpoint:** `/scoreboard`

**Method:** GET

**Query Parameters:**
- `year` (required): The year
- `month` (optional): The month
- `day` (optional): The day
- `limit` (optional): The maximum number of results (default: 100)

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if year is missing
- Error: 500 Internal Server Error if an error occurs

---

## Standings

Get the standings for a specific year and group.

**Endpoint:** `/standings`

**Method:** GET

**Query Parameters:**
- `year` (required): The year
- `group` (optional): The group (default: 'league'). Accepted values: 'league', 'conference', 'division'

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if year is missing or group is invalid
- Error: 500 Internal Server Error if an error occurs

---

## Team List

Get a list of teams.

**Endpoint:** `/team/list`

**Method:** GET

**Query Parameters:**
- `limit` (optional): The maximum number of results (default: 400)

**Response:**
- Success: 200 OK with JSON data
- Error: 500 Internal Server Error if an error occurs

---

## Team Info

Get information about a specific team.

**Endpoint:** `/team/info`

**Method:** GET

**Query Parameters:**
- `teamId` (required): The ID of the team

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if teamId is missing
- Error: 500 Internal Server Error if an error occurs

---

## Team Roster

Get the roster for a specific team.

**Endpoint:** `/team/roster`

**Method:** GET

**Query Parameters:**
- `teamId` (required): The ID of the team

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if teamId is missing
- Error: 500 Internal Server Error if an error occurs

---

## News

Get the latest news.

**Endpoint:** `/news`

**Method:** GET

**Query Parameters:**
- `limit` (optional): The maximum number of news items (default: 23)

**Response:**
- Success: 200 OK with JSON data
- Error: 500 Internal Server Error if an error occurs

---

## Player Season

Get the seasons for a specific player.

**Endpoint:** `/player/season`

**Method:** GET

**Query Parameters:**
- `playerId` (required): The ID of the player
- `page` (optional): The page number (default: 1)

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if playerId is missing
- Error: 500 Internal Server Error if an error occurs

---

## Player Leagues

Get the leagues for a specific player.

**Endpoint:** `/player/leagues`

**Method:** GET

**Query Parameters:**
- `playerId` (required): The ID of the player
- `page` (optional): The page number (default: 1)

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if playerId is missing
- Error: 500 Internal Server Error if an error occurs

---

## Player Statistics

Get statistics for a specific player.

**Endpoint:** `/player/statistic`

**Method:** GET

**Query Parameters:**
- `playerId` (required): The ID of the player

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if playerId is missing
- Error: 500 Internal Server Error if an error occurs

---

## Team Statistics Discipline

Get discipline statistics for a specific team.

**Endpoint:** `/team/statistic/discipline`

**Method:** GET

**Query Parameters:**
- `teamId` (required): The ID of the team
- `season` (optional): The season year (default: 2023)

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if teamId or season is missing
- Error: 500 Internal Server Error if an error occurs

---

## Team Statistics Scoring

Get scoring statistics for a specific team.

**Endpoint:** `/team/statistic/scoring`

**Method:** GET

**Query Parameters:**
- `teamId` (required): The ID of the team
- `season` (optional): The season year (default: 2023)

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if teamId or season is missing
- Error: 500 Internal Server Error if an error occurs

---

## Team Performance

Get performance data for a specific team.

**Endpoint:** `/team/perfomance`

**Method:** GET

**Query Parameters:**
- `teamId` (required): The ID of the team

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if teamId is missing
- Error: 500 Internal Server Error if an error occurs


## Team Transfers

Get transfer information for a specific team.

**Endpoint:** `/team/transfers`

**Method:** GET

**Query Parameters:**
- `teamId` (required): The ID of the team
- `season` (optional): The season year (default: 2023)
- `limit` (optional): The maximum number of results (default: 100)
- `page` (optional): The page number (default: 1)

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if required parameters are missing
- Error: 500 Internal Server Error if an error occurs

---

## Tables

Get tables for a specific season.

**Endpoint:** `/tables`

**Method:** GET

**Query Parameters:**
- `season` (optional): The season year (default: 2023)

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if season is missing
- Error: 500 Internal Server Error if an error occurs

---

## Injuries

Get injuries for the current season.

**Endpoint:** `/injuries`

**Method:** GET

**Response:**
- Success: 200 OK with JSON data
- Error: 500 Internal Server Error if an error occurs

---

## Team Results

Get results for a specific team in a given season.

**Endpoint:** `/team/results`

**Method:** GET

**Query Parameters:**
- `teamId` (required): The ID of the team
- `season` (optional): The season year (default: 2019)

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if teamId or season is missing
- Error: 500 Internal Server Error if an error occurs

---

## Player Overview

Get an overview of a specific player.

**Endpoint:** `/player/overview`

**Method:** GET

**Query Parameters:**
- `playerId` (required): The ID of the player

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if playerId is missing
- Error: 500 Internal Server Error if an error occurs

---

## Player Statistics

Get statistics for a specific player.

**Endpoint:** `/player/statistic`

**Method:** GET

**Query Parameters:**
- `playerId` (required): The ID of the player

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if playerId is missing
- Error: 500 Internal Server Error if an error occurs

---

## Player Bio

Get biographical information for a specific player.

**Endpoint:** `/player/bio`

**Method:** GET

**Query Parameters:**
- `playerId` (required): The ID of the player

**Response:**
- Success: 200 OK with JSON data
- Error: 400 Bad Request if playerId is missing
- Error: 500 Internal Server Error if an error occurs
