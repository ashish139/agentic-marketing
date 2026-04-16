cd d2c-marketing-platform

# 1. Install dependencies
pnpm install

# 2. Set up environment
cp .env.example .env
# Fill in SUPABASE_URL, SUPABASE_ANON_KEY, SUPABASE_SERVICE_ROLE_KEY, ANTHROPIC_API_KEY, OPENAI_API_KEY

# 3. Start Supabase locally
npx supabase start
npx supabase db push  # runs migrations
npx supabase db seed   # loads demo data

# 4. Start all services
pnpm dev  # or use docker-compose up
