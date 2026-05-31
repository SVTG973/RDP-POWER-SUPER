# 🚀 RDP-POWER SUPER - Free 6 hour Runner

> **Advanced GitHub Actions automation for RDP + Tailscale + RustDesk with FREE cycles-based 30-day continuous operation**

[![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-blue?logo=github)](https://github.com/features/actions)
[![Windows](https://img.shields.io/badge/Windows-0078D4?logo=windows)](https://www.microsoft.com/windows)
[![RustDesk](https://img.shields.io/badge/RustDesk-FF6B6B?logo=rust)](https://rustdesk.com)
[![Tailscale](https://img.shields.io/badge/Tailscale-00A3E0)](https://tailscale.com)
[![Cost](https://img.shields.io/badge/Cost-%24%200-green)]()

## ✨ Features

✅ **Completely FREE** - Uses GitHub Actions free tier minutes
✅ **30-Day Continuous** - Cycles-based workflow chaining
✅ **Multi-Instance** - 1-10 RDP instances simultaneously
✅ **Tailscale VPN** - Secure encrypted network access
✅ **RustDesk** - Remote desktop access with auto-screenshots
✅ **Chrome Remote Desktop** - Optional CRD support
✅ **Auto-Cleanup** - Automatic device purge at end

## 🚀 Quick Start

### Prerequisites
- GitHub Account with this repository
- Tailscale Account with:
  - API Key (device admin role)
  - Auth Key (reusable or ephemeral)
  - Tailnet name (your email)

### Setup (2 steps)

1. **Enable GitHub Actions**
   - Settings → Actions → General
   - ✅ "Allow all actions and reusable workflows"

2. **Run 30-Day Workflow**
   - Actions tab
   - Select: **RDP + Tailscale + RustDesk (A)**
   - Click: **Run workflow**
   - Enter:
     - `ts_tailnet`: your-email@gmail.com
     - `ts_api_key`: tskey-...
     - `ts_authkey`: tskey-...
     - `cycles`: **144** (for 30 days)
   - Click: **Run workflow** ✅

## 📋 Parameters

| Parameter | Default | Description |
|-----------|---------|-------------|
| `ts_tailnet` | - | Tailscale tailnet (required) |
| `ts_api_key` | - | API key (required) |
| `ts_authkey` | - | Auth key (required) |
| `cycles` | 0 | Workflow chain count: 144 = ~30 days FREE |
| `runtime_minutes` | 355 | Per-cycle runtime (5-360 min) |
| `rdp_count` | 1 | RDP instances (1-10) |
| `crd_code` | empty | Chrome Remote Desktop code |
| `crd_pin` | 123456 | CRD PIN (6-12 digits) |
| `do_purge` | true | Auto-purge old devices |
| `quick_test` | false | 5-min test mode |

## 💰 Cost

**$0 - Completely FREE!**

- Uses your GitHub free tier minutes
- Each cycle gets fresh free minutes
- No paid runners required

## 🔄 How It Works (Cycles)
Run Workflow A (355 min) ↓ Automatically dispatch Workflow B with cycles=N-1 ↓ Run Workflow B (355 min) ↓ Automatically dispatch Workflow A with cycles=N-2 ↓ ... continues until cycles=0 ↓ Dispatch STOP workflow to cleanup devices

**Example: `cycles: 144`**
- 144 cycles × 355 min ≈ 50,820 minutes
- ÷ 60 = 847 hours
- ÷ 24 = 35 days continuous operation
- **Cost: $0** ✅

## 📊 Usage Examples

### For 30 Days FREE

cycles: 144 runtime_minutes: 355 rdp_count: 1

### For 7 Days FREE

cycles: 30 runtime_minutes: 355

### For Quick Test

cycles: 0 quick_test: true

### Multi-Instance (3 RDP)

cycles: 50 rdp_count: 3

## 🔐 Security

⚠️ **Important:**
- Never commit credentials to repository
- Rotate API keys regularly
- Use ephemeral auth keys when possible
- Monitor Tailscale device list
- Check GitHub Actions logs for issues

## 📝 Logs

**View in GitHub:**
- Actions tab → Workflow run → Job logs

**Key Indicators:**
- ✅ Success steps
- ⚠️ Warnings/errors
- 🔄 Cycle chain dispatch status

## 🛠️ Troubleshooting

| Issue | Solution |
|-------|----------|
| Timeout | Reduce `runtime_minutes` to 300 |
| Tailscale fails | Verify API key & auth key format |
| RDP not accessible | Check Windows Defender firewall |
| CRD not working | Ensure code starts with `4/` |
| Cycles not chaining | Check GitHub token permissions |

## 📚 Files

- `.github/workflows/rdp-tailscale-rustdesk-A.yml` - Main workflow A
- `.github/workflows/rdp-tailscale-rustdesk-B.yml` - Alternate workflow B
- `.github/workflows/rdp-tailscale-stop.yml` - Cleanup workflow

## 🎯 Key Features

✅ **Windows Server** - Latest GitHub-hosted runner
✅ **Auto-Install** - RustDesk, Tailscale, Python libs
✅ **Auto-Screenshots** - Uploaded to Gofile
✅ **Heartbeat** - 60-sec monitoring during run
✅ **CRD Support** - Optional Chrome Remote Desktop
✅ **Auto-Cleanup** - Tailscale device purge

## 📖 Documentation

Based on original RDP-POWER by (THINKING XD)

Enhanced with:
- 30-day cycle support
- Better documentation
- Improved error handling

## ⚠️ Disclaimer

This tool is for legitimate testing and automation purposes only. Users are responsible for:
- GitHub Actions Terms of Service compliance
- Legal compliance in their jurisdiction
- Secure credential management
- System security

---

**Made with ❤️ for free GitHub Actions automation**

*Last Updated: 2025-05-30*
*Cost: $0 - Completely FREE* ✅
