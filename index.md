# Creating a minimal HTML structure as blank templates for each section
# These templates include only the essential structure, such as header, sidebar, main content, and footer

# Minimal HTML template structure
html_template = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Placeholder</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <!-- Header placeholder -->
    </header>
    
    <nav>
        <!-- Sidebar placeholder -->
    </nav>
    
    <main>
        <!-- Main content placeholder -->
    </main>
    
    <footer>
        <!-- Footer placeholder -->
    </footer>
</body>
</html>
"""

# Creating multiple HTML pages as blank templates, which mimic the structure without any actual content
# Save each template as separate files, representing different pages of the documentation site

pages = ["home", "getting_started", "tutorial", "api_reference", "guide", "faq", "about"]
file_paths = []

for page in pages:
    file_path = f"/mnt/data/{page}.html"
    with open(file_path, "w") as file:
        file.write(html_template.replace("Page Placeholder", page.replace("_", " ").title()))
    file_paths.append(file_path)

file_paths