import os

def create_roadmap_structure(base_dir):
    categories = [
        "frontend_development",
        "backend_development",
        "devops",
        "data_science",
        "mobile_development",
        "machine_learning",
        "cybersecurity",
        "blockchain",
        "game_development"
    ]
    
    os.makedirs(base_dir, exist_ok=True)
    for category in categories:
        os.makedirs(os.path.join(base_dir, category), exist_ok=True)
        with open(os.path.join(base_dir, category, "README.md"), "w") as f:
            f.write(f"# {category.replace('_', ' ').title()} Roadmap\n\n")
    
    with open(os.path.join(base_dir, "README.md"), "w") as f:
        f.write("# Developer Roadmap\n\nA structured roadmap for different developer roles.\n")
    
    print(f"Developer roadmap structure created in '{base_dir}'")

if __name__ == "__main__":
    create_roadmap_structure("developer_roadmap")
# developer-roadmap
