# workshop

**export the databse**
`
export DATABASE_URL=postgresql://postgres:postgres@localhost/practice
`

**To create the geometry**

`
ALTER TABLE public.five_year
ADD COLUMN geometry geometry(Polygon, 4326) 
GENERATED ALWAYS AS (h3_cell_to_boundary_geometry(h3_ix)) STORED;
`


**To create index**

`
CREATE INDEX idx_five_year_geometry 
ON five_year 
USING GIST (geometry);
`

**to start the server**

`

uvicorn main:app --reload
`


**vcpu + core concept**

**Rule of thumb**
**worker**
**lamda function**
`
https://geoparquet.org/
`
**flatgeobuff**
**R2 cloud**

**symantic versioning**
**https://semver.org/**

**speed of cloud memory**


**env variable**

**terminal large query**


**screen session  on server**

sudo bash pre.sh

**compact h3 grid**

**for different level h3 index use of hierarchy**
**find the parent and childern**

max zoom is connectedd to h3

read and write of dics(ops speed) for writing tile

fiona shapely vs gdal




Devops



htop to view all the data



shotbot for hhtps

cloudfare 

nginex

jwt auth


sql injetction


