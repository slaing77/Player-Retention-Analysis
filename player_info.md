SELECT
DISTINCT pi.player_id,
location,
age AS age_at_signup,
system,
pi.joined,
m.outcome,
MAX(m.day) AS last_match,
COUNT(pu.item_id) AS purchases,
ii.price
FROM
  `heroic-district-329518.gamecompanydata.player_info`  AS pi
INNER JOIN `heroic-district-329518.gamecompanydata.matches_info` m
ON Pi.player_id = m.player_id
INNER JOIN `heroic-district-329518.gamecompanydata.purchase_info` pu
ON Pi.player_id = pu.player_id
INNER JOIN `heroic-district-329518.gamecompanydata.item_info` ii
ON pu.item_id = ii.item_id
group by 1,2,3,4,5,6,9
ORDER BY pi.joined 
LIMIT 1000
 