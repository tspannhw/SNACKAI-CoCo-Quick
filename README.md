## SQL

````




select * from demo.demo.WEATHER_OBSERVATIONS_C ;


SELECT * from demo.demo.planes order by ts desc;


select * from "DEMO"."DEMO"."MANHATTAN_CAMERA_LIST";

CALL "DEMO"."DEMO"."ANALYZETRAFFICIMAGE"('${filename}','${filename}','${videoid}');

select * from DEMO.DEMO.NYCTRAFFICIMAGES order by CREATED_TS DESC;


    select * from SNOWFLAKE.LOCAL.CORTEX_ANALYST_REQUESTS_V
order by timestamp desc;


LIST @DEMO.DEMO.SLACKIMAGES;
LIST @DEMO.DEMO.TRAFFIC;


select * from demo.demo.weather_observations order by updated_at desc;

select * from demo.demo.AIR_QUALITY_DATA_SF order by datetimeto desc;

CALL "DEMO"."DEMO"."ANALYZESLACKIMAGE"('${filename}','${filename}','${videoid}');

select * from demo.demo.SLACKIMAGES order by ts desc;

SELECT symbol as symbol FROM DEMO.DEMO.STOCK;

select * from demo.demo.stockvalues;

-- https://docs.snowflake.com/en/user-guide/data-engineering/row-timestamps

select *
from demo.demo.ICYMTA
order by ts desc
LIMIT 500;

    select * from rawnyctrafficimages;

    select * from VWRAWTRAFFIC;

    SELECT AI_REDACT(
input => 'My name is Tim Spann and I live at twenty third street, New York, NY.'
);


show semantic views;
describe semantic view traffic;

select * from semantic_view(vwrawtraffic METRICS vwrawtraffic.image_text);


WITH __nyctrafficimages AS (
  SELECT
    roadwayname,
    created_ts
  FROM demo.demo.nyctrafficimages
)
SELECT
  COUNT(*) AS image_count
FROM __nyctrafficimages
WHERE
  roadwayname = 'I-87 - NYS Thruway'
  AND created_ts >= DATE_TRUNC('MONTH', DATEADD(MONTH, -6, CURRENT_DATE))
  AND created_ts <= DATE_TRUNC('MONTH', CURRENT_DATE)
ORDER BY
  created_ts DESC NULLS LAST;

select roadwayname, image_text from VWTRAFFICIMAGEFORSEARCH;

select * from DEMO.DEMO.VWRAWTRAFFIC;

SELECT (LATITUDE) as Latitude,(LONGITUDE) as Longitude,ROADWAYNAME,VIDEONAME,DIRECTIONOFTRAVEL,FILENAME
FROM DEMO.DEMO.NYCTRAFFICIMAGES
WHERE LATITUDE IS NOT NULL 
AND LONGITUDE IS NOT NULL;

select * FROM DEMO.DEMO.NYCTRAFFICIMAGES
WHERE LATITUDE IS NOT NULL 
AND LONGITUDE IS NOT NULL;

delete from  DEMO.DEMO.NYCTRAFFICIMAGES
where videoname is null or TRIM(VIDEONAME) = '';

    SELECT
    roadwayname,
    DATE_TRUNC('MONTH',created_ts), created_ts,DATE_TRUNC('MONTH', CURRENT_DATE), *
  FROM demo.demo.nyctrafficimages
  where roadwayname = 'I-87 - NYS Thruway';
  

````
