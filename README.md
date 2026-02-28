sudo -u postgres psql
\c nexusdb2
\dx
or run
SELECT * FROM pg_extension WHERE extname = 'pg_trgm';
