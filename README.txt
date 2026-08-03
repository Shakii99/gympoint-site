GYMPOINT - RECUPERO PASSWORD

1) In ENTRAMBI i file sostituisci:
   INSERISCI_SUPABASE_URL
   INSERISCI_SUPABASE_PUBLISHABLE_KEY
   con URL e Publishable/anon key del progetto Supabase.
   NON usare mai la service_role key.

2) Carica i file nel repository gympoint-site.

URL finali:
https://shakii99.github.io/gympoint-site/forgot-password.html
https://shakii99.github.io/gympoint-site/reset-password.html

3) Supabase Dashboard -> Authentication -> URL Configuration
Aggiungi tra i Redirect URLs:
https://shakii99.github.io/gympoint-site/reset-password.html

4) Flusso:
forgot-password.html -> invia email tramite resetPasswordForEmail -> link Supabase -> reset-password.html -> updateUser(password).
