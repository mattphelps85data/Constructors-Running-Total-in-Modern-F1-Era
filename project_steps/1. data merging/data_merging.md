
# Step 1: Data Merging

I imported the Formula 1 World Championship (1950 - 2023) dataset from Kaggle.

https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020


## Import Dataset 

Create SQL tables then import in pgAdmin4.

note: Changed constructors.csv file name to teams.csv

```bash
  -- Table: public.races

-- DROP TABLE IF EXISTS public.races;

CREATE TABLE IF NOT EXISTS public.races
(
    "raceId" integer NOT NULL,
    "circuitId" integer,
    name character varying(50) COLLATE pg_catalog."default",
    date date,
    CONSTRAINT races_pkey PRIMARY KEY ("raceId")
)

TABLESPACE pg_default;

ALTER TABLE IF EXISTS public.races
    OWNER to postgres;
	
-- Table: public.results

-- DROP TABLE IF EXISTS public.results;

CREATE TABLE IF NOT EXISTS public.results
(
    "resultID" integer NOT NULL,
    "raceId" integer,
    "constructorId" integer,
    points numeric,
    CONSTRAINT results_pkey PRIMARY KEY ("resultID")
)

TABLESPACE pg_default;

ALTER TABLE IF EXISTS public.results
    OWNER to postgres;

-- Table: public.teams

-- DROP TABLE IF EXISTS public.teams;

CREATE TABLE IF NOT EXISTS public.teams
(
    "constructorId" integer NOT NULL,
    team_name character varying(50) COLLATE pg_catalog."default",
    CONSTRAINT teams_pkey PRIMARY KEY ("constructorId")
)

TABLESPACE pg_default;

ALTER TABLE IF EXISTS public.teams
    OWNER to postgres;
```
    
## Join Tables

Joined results table for points, teams table for constructor names, and races table for races and dates.

```bash
SELECT 
	races."date",
	results."points",
	teams."team_name" 
FROM results
LEFT JOIN races
ON results."raceId"=races."raceId"
LEFT JOIN teams
ON results."constructorId"=teams."constructorId";
```

Then save file as "jointable.csv" file 