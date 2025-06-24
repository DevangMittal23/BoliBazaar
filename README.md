# BoliBazaar - Voice-Based Auction Website

# Its Updated repo is : 
https://github.com/sanatanisher01/Boli

A modern auction platform with voice-powered bidding capabilities built with Django.

## 🎥 Demo Video
[![BoliBazaar Demo](https://img.youtube.com/vi/Znipo2gjlhw/0.jpg)](https://www.youtube.com/watch?v=Znipo2gjlhw)

## 🎯 Features

### User Roles
- **Public Users**: Register, browse auctions, place bids via voice or manual input
- **Admin Users**: Manage products, view bids, generate reports

### Core Features
- **Voice Commands**: 
  - "What is the current bid on [Product Name]?"
  - "Place a bid of [Amount] rupees on [Product Name]"
- **Real-time Updates**: Live countdown timers and bid updates
- **Responsive Design**: Works on desktop and mobile
- **Dark/Light Theme**: Toggle between themes
- **Report Generation**: PDF and CSV reports for admins

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- pip

### Installation

1. **Clone/Download the project**
   ```bash
   cd BoliBazaar
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up the database**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

4. **Create sample data**
   ```bash
   python setup.py
   ```

5. **Start the server**
   ```bash
   python manage.py runserver
   ```

6. **Visit the website**
   Open http://127.0.0.1:8000 in your browser

## 👥 Login Credentials

### Admin Account
- **Username**: admin
- **Password**: admin123
- **Access**: Full admin dashboard, product management, reports

### Demo User Account
- **Username**: demo
- **Password**: demo123
- **Access**: Regular user features, bidding

## 🎤 Voice Commands

### Supported Commands
1. **Check Current Bid**
   - "What is the current bid?"
   - "What is the current bid on [Product Name]?"

2. **Place Bid**
   - "Place a bid of [amount] rupees"
   - "Place a bid of [amount] rupees on [Product Name]"

### Using Voice Features
1. Click the microphone button on product detail pages
2. Wait for the "Listening..." prompt
3. Speak clearly in English
4. The system will process your command and respond

## 📱 User Guide

### For Regular Users
1. **Register**: Create account with name, email, password
2. **Browse**: View active auctions on homepage
3. **Bid**: Click on products to view details and place bids
4. **Dashboard**: Track your bidding history and status

### For Admins
1. **Login**: Use admin credentials
2. **Add Products**: Create new auction items
3. **Manage**: Edit or delete existing products
4. **Reports**: Generate PDF/CSV reports of all auctions
5. **Monitor**: View all bids and auction status

## 🛠️ Technical Details

### Built With
- **Backend**: Django 4.2.7
- **Frontend**: HTML5, CSS3, JavaScript, Bootstrap 5
- **Database**: SQLite (default)
- **Voice**: Web Speech API
- **Reports**: ReportLab (PDF), CSV

### Project Structure
```
BoliBazaar/
├── auction/                 # Main app
│   ├── models.py           # Database models
│   ├── views.py            # Business logic
│   ├── forms.py            # Form definitions
│   └── urls.py             # URL routing
├── templates/              # HTML templates
│   ├── base.html          # Base template
│   ├── auction/           # App templates
│   └── registration/      # Auth templates
├── static/                # Static files
├── media/                 # Uploaded files
└── manage.py              # Django management
```

### Key Models
- **Product**: Auction items with title, description, price, end time
- **Bid**: User bids with amount, timestamp, bidder info
- **User**: Django's built-in user model extended with profiles

## 🔧 Customization

### Adding New Features
1. Modify models in `auction/models.py`
2. Create/update views in `auction/views.py`
3. Add URL patterns in `auction/urls.py`
4. Create templates in `templates/auction/`

### Styling
- Edit `templates/base.html` for global styles
- Bootstrap 5 classes are available throughout
- Custom CSS can be added to the base template

### Voice Commands
- Extend `processVoiceCommand()` function in product detail template
- Add new command patterns and responses
- Modify speech recognition settings as needed

## 🚨 Troubleshooting

### Common Issues

1. **Voice not working**
   - Ensure you're using HTTPS or localhost
   - Check browser microphone permissions
   - Try Chrome/Edge browsers for best compatibility

2. **Images not displaying**
   - Check MEDIA_URL and MEDIA_ROOT settings
   - Ensure media directory has proper permissions

3. **Database errors**
   - Run `python manage.py makemigrations`
   - Run `python manage.py migrate`
   - Delete db.sqlite3 and recreate if needed

### Browser Compatibility
- **Voice Features**: Chrome, Edge, Safari (latest versions)
- **General Features**: All modern browsers
- **Mobile**: Responsive design works on all devices

## 📄 License

This project is created for educational purposes. Feel free to modify and use as needed.

## 🤝 Contributing

1. Fork the project
2. Create feature branch
3. Make changes
4. Test thoroughly
5. Submit pull request

## 📞 Support

For issues or questions:
1. Check the troubleshooting section
2. Review Django documentation
3. Check browser console for JavaScript errors

---

**Happy Bidding! 🎉**
