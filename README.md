# Keep‑alive Pinger

A GitHub Actions workflow to keep your web services alive. It pings the specified URLs every 25 minutes to prevent them from going to sleep (useful for services like the Render free plan).

## 🛠 Як користуватись

1. Fork or clone this repository.
2. :Edit the `.github/workflows/ping.yml`, file and add your own URLs:
   ```yaml
   curl -m 10 -s https://your-backend-url/api || echo "Ping failed"
   curl -m 10 -s https://your-frontend-url || echo "Ping failed"
