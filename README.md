Linux Permissions Project – Real-World Business Application

This repository is not based on a fictional scenario. It is a real implementation of Linux file ownership and permissions for a live, active online business.

Business Context:
My wife and I run an educational YouTube channel with 644,251 subscribers (gaining over 10,000 new subscribers in the last 28 days) focused on teaching English to learners across the MENA (Middle East and North Africa) region.

The channel delivers accessible, culturally-aware ESL content covering:
    Financial English
    Technology & IT English
    Tourism & Workplace English
    And more coming soon (listening, gamified content, PDFs, etc.)
    The Next Phase – ESL Website + Listening Library
We’re now building a complementary website that will host a growing MP3-based English listening library, organised by category and controlled through Linux permissions. The goal is to securely manage content uploads and team collaboration using open-source tools.


 Linux Use Case Summary

This part of the project uses Linux to:
    Create a structured folder system for audio libraries (e.g., Business English, Tech English)
    Assign ownership to admin team members using chown
    Control permissions for:
        Owner (main creator)
        Group (admin team collaborators)
        Others (students with read-only access)

        # Create nested directories for the MP3 library
mkdir -p ~/ESL_website/mp3_library/{business_english,tech_english,tourism_english}

Create admin team group and add collaborators
sudo groupadd adminteam
sudo usermod -aG adminteam fatima

Change ownership of the library to user and group
sudo chown gary:adminteam mp3_library

Set permissions: for owner, read/write for group, and read-only for others
chmod 764 mp3_library

Why This Matters

I'm not just playing with Linux — I'm using it in production to:
    Secure real student-facing learning content
    Collaborate with my wife as a growing team
    Lay the technical foundation for a scalable education platform
    Manage future services like automatic uploads, cron-based backups, and version-controlled lessons


    What Comes Next
    Shell scripts to automate folder creation and permission control
    cron jobs for scheduled uploads or backups
    GitHub actions to link website development with version control
