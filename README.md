# Advanced Blog Platform

**Author:** Taha Nawaz
**Email:** su92-bsefm-f24-004
**Professor:** Irum Fatima

---

## Project Overview

**Advanced Blog** is a fully-featured blogging platform built with **Django**. It includes advanced features such as **user authentication, role-based permissions, post management, comments, categories, tags, search, and image uploads**. This project demonstrates how to build scalable web applications using Django’s ecosystem.

---

## Features

### User Roles

* **Admin:** Full access to all posts, comments, categories, tags, and users.
* **Author:** Can create, edit, and delete their own posts.
* **Reader:** Can view posts and add comments.

### Blog Features

* Create, edit, and delete posts with **Draft/Published status**.
* Assign posts to **categories** and **tags**.
* Rich text content support for posts using **CKEditor**.
* Upload images for posts.
* SEO-friendly **slug-based URLs**.
* Pagination on homepage.
* Filter posts by **category** or **tag**.
* Search posts by **title** or **content**.

### Comment System

* Users can comment on posts.
* Optional: comment moderation feature can be added.

### Author Dashboard

* Authors can manage their posts easily.

### Admin Panel

* Manage posts, categories, tags, and comments.
* Full access for superusers.

---

## Installation

1. **Clone the repository**

```bash
git clone <repository-url>
cd advanced_blog
```

2. **Create virtual environment**

```bash
python -m venv myenv
myenv\Scripts\activate      # Windows
source myenv/bin/activate   # macOS/Linux
```

3. **Install dependencies**

```bash
pip install django
pip install pillow
pip install django-ckeditor
```

4. **Apply migrations**

```bash
python manage.py makemigrations
python manage.py migrate
```

5. **Create superuser**

```bash
python manage.py createsuperuser
```

6. **Run the development server**

```bash
python manage.py runserver
```

Open your browser at [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

---

## Usage

* **Homepage:** view all published posts.
* **Post detail page:** view full content and comments.
* **Author Dashboard:** manage your posts (`/dashboard/`).
* **Categories & Tags:** filter posts by category or tag.
* **Search:** search posts by keywords.

---

## Deployment

* Set `DEBUG = False` in `settings.py`.
* Add `ALLOWED_HOSTS = ['your-domain.com']`.
* Configure static and media files for production.
* Push your code to your hosting platform.

---

## Database Schema

**Tables:**

1. **User** (Django built-in)
2. **Post**: title, slug, content, author (FK: User), category (FK: Category), tags (M2M: Tag), status (Draft/Published), image, created_at, updated_at
3. **Category**: name, slug
4. **Tag**: name, slug
5. **Comment**: post (FK: Post), user (FK: User), content, created_at

---


## Author

**Taha Nawaz** 

