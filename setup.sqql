### 2. SQL Database Integration (Supabase Setup)

Your JavaScript code pushes flower objects to a `flowers` table in Supabase[cite: 1]. Based on the data structure in your code (`id`, `dataUrl`, `x`, `y`, `w`, `h`, `ownerId`, `isLocked`), here is the exact SQL you need to create the table.

Create a folder named `sql` in your repository and add a file named `schema.sql` inside it. Paste the following SQL code into that file. You will also need to copy and paste this code into the **SQL Editor** in your Supabase dashboard and hit "Run".

```sql
-- Create the flowers table
CREATE TABLE flowers (
    id TEXT PRIMARY KEY,
    "dataUrl" TEXT NOT NULL,
    x FLOAT NOT NULL,
    y FLOAT NOT NULL,
    w FLOAT NOT NULL,
    h FLOAT NOT NULL,
    "ownerId" TEXT NOT NULL,
    "isLocked" BOOLEAN DEFAULT FALSE
);

-- Enable Realtime for the flowers table
-- This allows your JavaScript channel ('public:flowers') to listen for inserts, updates, and deletes
ALTER PUBLICATION supabase_realtime ADD TABLE flowers;

-- Set up Row Level Security (RLS)
-- Note: Since this is a public canvas, we are allowing open access. 
-- If you want to restrict this later, you will need to modify these policies.
ALTER TABLE flowers ENABLE ROW LEVEL SECURITY;

-- Allow anyone to read flowers
CREATE POLICY "Allow public read access" 
ON flowers FOR SELECT 
USING (true);

-- Allow anyone to insert new flowers
CREATE POLICY "Allow public insert access" 
ON flowers FOR INSERT 
WITH CHECK (true);

-- Allow anyone to update flowers
CREATE POLICY "Allow public update access" 
ON flowers FOR UPDATE 
USING (true);

-- Allow anyone to delete flowers
CREATE POLICY "Allow public delete access" 
ON flowers FOR DELETE 
USING (true);
