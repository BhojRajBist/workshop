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




