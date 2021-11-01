SELECT
  location,
  pi.player_id,
  age AS age_at_signup,
  system,
  joined,
  m.outcome,
FROM
  `heroic-district-329518.gamecompanydata.player_info` AS Pi
JOIN
  `heroic-district-329518.gamecompanydata.matches_info` M
ON
  Pi.player_id = M.player_id
GROUP BY
  1,
  2,
  3,
  4,
  5,
  6
ORDER BY
  joined DESC
LIMIT
  1000
 
