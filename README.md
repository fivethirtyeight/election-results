# election-results

These files contain up-to-date results of elections for Governor, U.S. Senate, and President (including primaries), both nationally and by state, from the November 1998 general election to the present.

## election_results files

Column | Description
-------|------------
`id` | 538 database id for the result
`race_id` | 538 database id for the corresponding race (see `races.csv` for race details)
`state_abbrev` | Standard state abbreviation for the race. If blank, race is national.
`state` | Full name of the state. If blank, race is national.
 `office_id` | 538 database id for the corresponding office.
 `office_name` | Name of office; either U.S. Senate, U.S. House, Governor, or President.
 `office_seat_name` | Name of the corresponding seat. For U.S. Senate races, this will note the class of the senate seat. For U.S. House races, this will note the district number.
 `cycle` | Cycle of the corresponding race
 `stage` | Stage of the corresponding race: either general, primary, caucus, jungle primary, or runoff
 `special` | `true` or `false` depending on if the race is a special election
 `party` | Indicates the party of the race. For primaries, this should read `DEM` or `REP`; for non-primaries, this should be blank
 `politician_id` | 538 database id for the politician.
 `candidate_id` | 538 database id for the candidate. A candidate is a politician, who is running for a particular office in a particular year. For example, Donald Trump two separate `candidate_id`s for his 2016 and 2020 runs for president, but only one `politician_id`.
 `candidate_name` | Name of the corresponding candidate.  If blank, the result is not for a particular candidate (e.g., Write-in votes that are not disambiguated by candidates)
 `ballot_party` | Party under which the candidate appears on the ballot for this race.
 `votes` | Number of votes for the candidate. If blank, indicates that the race is not one for which votes are available (e.g., a national presidential primary)
 `percent` | Percent of votes for the candidate. If blank, indicates that the race is not one for which votes are available (e.g., a national presidential primary)
 `unopposed` | Flag for whether the candidate ran unopposed, and results are unavailable.
  `winner` | true/false flag for whether the candidate won the corresponding election
  `alt_result_text` | If the result is not about a particular candidate, text of the result (e.g., Scattering, Blank, Write-in)
  `source` | Source from which 538 gathered this data.
  

## `races.csv`

Column | Description
-------|------------
`id` | 538 database id for the race
`type` | Type of race: either `SenateRace`, `GubernatorialRace`, `PresidentialRace`, `HouseRace`, `GenericHouseRace`, or `MayoralRace`
`state_abbrev` | Standard state abbreviation for the race. If blank, race is national.
`State` | Full name of the state. If blank, race is national.
`office_id` | 538 database id for the corresponding office.
`office_name` | Name of office; either U.S. Senate, U.S. House, Governor, Mayor, or President.
`office_seat_name` | Name of the corresponding seat. For U.S. Senate races, this will note the class of the senate seat. For U.S. House races, this will note the district number.
`cycle` | Cycle of the corresponding race
`stage` | Stage of the corresponding race: either general, primary, caucus, jungle primary, or runoff
`special` | true/false flag for whether the race is a special election
`incumbent_party` | Indicates the party of the politician that held the seat at the time of the race. If the seat was vacant at the time of the race, this will be blank.
`party` | Indicates the party of the race. For primaries, this should read `DEM` or `REP`; for non-primaries, this should be blank
`date` | Date on which the race was held. If blank, the race either did not occur (e.g., a runoff that was not needed) or represents a national primary that occurs on several different dates in different states
`created_at` | Timestamp for when the race was added to the 538 database
`updated_at` | Timestamp for when the race was last updated in the 538 database
