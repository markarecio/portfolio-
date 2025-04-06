# portfolio-
class Resume:
    def __init__(self, name, location, phone, email, portfolio, summary, skills, experience, education):
        self.name = name
        self.location = location
        self.phone = phone
        self.email = email
        self.portfolio = portfolio
        self.summary = summary
        self.skills = skills
        self.experience = experience
        self.education = education

    def print_resume(self):
        print(f"{self.name}")
        print(f"{self.location} | {self.phone} | {self.email} | {self.portfolio}")
        print("\nProfessional Summary")
        print(self.summary)
        print("\nKey Skills")
        for skill in self.skills:
            print(f"● {skill}")
        print("\nProfessional Experience")
        for role in self.experience:
            print(f"{role['title']} | {role['company']} | {role['dates']}")
            for responsibility in role['responsibilities']:
                print(f"  - {responsibility}")
        print("\nEducation & Certifications")
        for edu in self.education:
            print(f"{edu['degree']} – {edu['institution']}, {edu['location']}")
            if 'certifications' in edu:
                print("Relevant Certifications:")
                for cert in edu['certifications']:
                    print(f"● {cert}")


if __name__ == "__main__":
    resume = Resume(
        name="Mark Anthony Recio",
        location="Las Vegas, NV",
        phone="(702) 717-1198",
        email="recio.mark.a@gmail.com",
        portfolio="https://markareciocareerpath.my.canva.site/portfolio",
        summary="Data-driven business professional with expertise in data analysis, business analytics, and HR operations. "
                "Skilled in leveraging analytical tools to derive insights, optimize processes, and support strategic decision-making. "
                "Adept at stakeholder management, project execution, and data visualization.",
        skills=[
            "Data Analysis & Visualization: Google Analytics, Power BI, Tableau, SQL, R, Python",
            "Business Analytics: Financial analysis, KPI tracking, process optimization",
            "HR & Operations: Talent acquisition, payroll analysis, employee performance metrics",
            "Communication & Reporting: Data storytelling, executive reporting, presentation skills"
        ],
        experience=[
            {
                'title': 'Independent Contractor',
                'company': 'DataTalent Pro',
                'dates': 'August 2023 – Present',
                'responsibilities': [
                    'Conduct data-driven analysis to optimize candidate sourcing and hiring strategies.',
                    'Web scrape resumes and HR data to analyze for top talent applicants using Python.',
                    'Use a matrix to evaluate and rank candidates based on criteria.',
                    'Utilize Power BI to track and visualize recruitment metrics, improving hiring efficiency.',
                    'Conducted data analytics using Google Analytics to analyze website consumer behavior performance and provide insight recommendations for new marketing campaigns.'
                ]
            },
            {
                'title': 'Operations Manager Assistant',
                'company': 'Bella Brite Services',
                'dates': 'October 2018 – August 2023',
                'responsibilities': [
                    'Analyzed payroll data to improve accuracy and reduce processing time by 20%.',
                    'Implemented employee scheduling, reducing conflicts and enhancing productivity.',
                    'Developed an inventory tracking system, increasing supply chain efficiency.'
                ]
            }
        ],
        education=[
            {
                'degree': 'Master of Business Administration (MBA)',
                'institution': 'Keller Graduate School of Management',
                'location': 'CA'
            },
            {
                'degree': 'Graduate Certificate in Strategic Innovation & Change',
                'institution': 'University of Denver',
                'location': 'CO',
                'certifications': [
                    "IBM Data Analyst – IBM",
                    "Microsoft Power BI Data Analyst – Microsoft",
                    "BI Essentials for Finance Analyst (Power BI Edition) – Corporate Finance Institute",
                    "Financial Analysis: Skills for Success – University of Illinois",
                    "Business Analytics with R Programming – University of Illinois",
                    "R Programming for Statistics and Data Science – Packt",
                    "Data Science Math Skills – Duke University"
                ]
            }
        ]
    )

    resume.print_resume()
