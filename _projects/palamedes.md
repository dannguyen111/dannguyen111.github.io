---
layout: project
title: "Palamedes: Fraternity Management Platform"
description: "A comprehensive web application built with Django to streamline chapter operations, point tracking, and financial dues for Greek life organizations."
image: "/assets/images/palamedes-preview.png"
date: 2026-02-17
---

## Project Overview
Managing a fraternity chapter involves juggling multiple moving parts: member rosters, financial dues, and activity points. Drawing from firsthand leadership experience managing chapter operations, I developed **Palamedes**—a centralized, multi-tenant web platform designed to simplify Greek life administration. 

The application allows organizations to dynamically register their chapters, onboard members via secure invite codes, and delegate management tasks through a strict hierarchical permission system. The site is currently deployed live and actively routing real-world traffic.

## Technical Approach

### 1. Role-Based Access Control (RBAC)
To handle the complex hierarchy of a fraternity, I engineered a highly customized user and position model system.
- **Hierarchical Permissions:** Users are assigned granular boolean permissions (e.g., `can_manage_finance`, `can_manage_nm_points`) based on their elected executive roles.
- **Automated Onboarding:** Implemented a secure registration pipeline where the chapter President receives separate generated invite codes for Actives and New Members, automatically routing new sign-ups to the correct status and chapter ledger.

### 2. Financial Management & Stripe Integration
A major friction point for chapters is collecting and tracking dues. I built a comprehensive financial dashboard for Treasurers.
- **Bulk & Individual Billing:** Executives can query the chapter directory and issue single or bulk charges to specific members, pledge classes, or statuses.
- **Stripe API:** Integrated Stripe Checkout to process payments securely. The backend utilizes custom metadata passing to listen for successful session webhooks and automatically update a member's outstanding balance in the database.

### 3. Activity Point Tracking Engine
I developed a "Points Hub" to incentivize and track member participation.
- **Interactive Ledgers:** Built dynamic data tables that sort and filter point requests by recipient, approver, and status.
- **Workflow Approvals:** Members can submit point requests that route directly to the designated executive's queue for approval, rejection, or counter-offers. Executives have specialized inline tools to safely audit and edit historical logs.

## Key Technologies
* **Framework:** Django (Python)
* **Frontend:** Bootstrap 4, HTML/CSS, JavaScript (jQuery)
* **Database & Storage:** PostgreSQL, AWS S3 (boto3, django-storages)
* **Payments:** Stripe API
* **Deployment:** Render, Gunicorn, WhiteNoise

[Visit Palamedes Live](https://palamedes.xyz){: .btn .btn-primary .mt-3}

[View Code on GitHub](https://github.com/dannguyen111/palamedes){: .btn .btn-outline-primary .mt-3}