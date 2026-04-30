📇 Contact App
A simple, modern Android contact manager built with Kotlin.
Browse your contacts in a clean list, view their details,
and quickly call or text them — all in a lightweight and intuitive interface.

Feature	Description
📋 Contact List	Displays contacts in a RecyclerView with circular avatars and clean layout
👤 Detail Screen	Shows full name, phone number, and profile image of the selected contact
📞 Direct Call	Opens the phone dialer with the contact's number pre-filled
💬 Send SMS	Opens the messaging app with the contact's number ready to go
📱 Edge-to-Edge	Full-screen experience using enableEdgeToEdge()
🔄 RTL Support	Fully compatible with right-to-left languages like Persian and Arabic
🔒 API Compatibility	Smart Parcelable handling for both Android 13+ and older versions
🏗 Project Structure
text

📦 com.example.contact
├── 📄 MainActivity.kt              ← Main screen (contact list)
├── 📄 DetailContact.kt             ← Detail screen (contact info + actions)
├── 📄 ContactAdapter.kt            ← RecyclerView adapter
└── 📁 model/
    └── 📄 Contact.kt               ← Data model (@Parcelize)

📦 res/layout
├── 📄 activity_main.xml            ← Main screen layout
├── 📄 activity_detail_contact.xml  ← Detail screen layout
└── 📄 item_contact.xml             ← Single contact item layout

🛠 Tech Stack
Technology	Detail
Language	Kotlin
UI	XML + ConstraintLayout
View Binding	✅ Enabled
RecyclerView	LinearLayoutManager
Data Passing	Parcelable (kotlinx.parcelize)
Circular Image	CircleImageView
Min SDK	API 21 (Android 5.0)
Target SDK	API 31 (Android 12)
IDE	Android Studio
📐 App Flow
┌─────────────────────┐
│    MainActivity      │
│   (Contact List)     │
│                      │
│   ┌──────────────┐   │
│   │  Item Click  │───┼────────────┐
│   └──────────────┘   │            │
└─────────────────────┘            │
                                    ▼
                        ┌──────────────────────┐
                        │    DetailContact      │
                        │                       │
                        │   👤 Name + Phone     │
                        │                       │
                        │  ┌────────┐ ┌──────┐  │
                        │  │  Call  │ │ SMS  │  │
                        │  └───┬────┘ └──┬───┘  │
                        └──────┼─────────┼──────┘
                               │         │
                               ▼         ▼
                          Phone App   SMS App
