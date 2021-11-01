
SELECT
 joined_day,
  COUNT (DISTINCT player_id ) total_players, -- count all unique player_id's to get total
  SUM(retained) / COUNT(DISTINCT player_id) AS retention_rate,
 
FROM (
  SELECT -- to identify each players join date, last game so we can identify n retained and calc. retention rate
    player_id,
    last_game,
    joined_day,
    outcome,
    last_game-joined_day AS dif, --the amount of days between a player joining and theit last game played
    CASE
      WHEN last_game-joined_day <=30 THEN 1 -- assigning a numerical value for all the players who were still engaged on day 30 
    ELSE -- assigning a numerical value for all players who were not still engaged 30 days in
    0
  END
    AS retained -- shows the number of retained players at 30 days
  FROM (
    SELECT
      a.player_id,
      MAX(b.day) last_game,
      joined AS joined_day,
      b.outcome
    FROM
      heroic-district-329518.gamecompanydata.player_info AS a
    JOIN
      heroic-district-329518.gamecompanydata.matches_info b
    ON
      a.player_id=b.player_id
    GROUP BY
      player_id,
      b.outcome,
      joined_day,
      b.outcome
    )) -- end of nesting
GROUP BY 
joined_day