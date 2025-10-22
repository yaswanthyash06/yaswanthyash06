import developerIllustration from "@/assets/developer-illustration.jpg";

const About = () => {
  return (
    <section id="about" className="py-20 px-4 bg-secondary/30">
      <div className="max-w-5xl mx-auto">
        <h2 className="text-3xl md:text-4xl font-bold mb-12 text-center">About Me</h2>
        <div className="grid md:grid-cols-2 gap-8 items-center">
          <div className="space-y-4 text-muted-foreground leading-relaxed">
          <p className="text-lg">
            I'm currently pursuing my Master of Computer Applications (MCA), where I'm deepening my 
            understanding of software development, algorithms, and system design. My academic journey 
            has equipped me with a strong foundation in multiple programming languages and database technologies.
          </p>
          <p className="text-lg">
            I'm particularly interested in developing robust applications that solve real-world problems. 
            Through my coursework and personal projects, I've gained hands-on experience in various aspects 
            of software development, from front-end design to back-end architecture.
          </p>
          </div>
          <div className="flex justify-center">
            <img 
              src={developerIllustration} 
              alt="Developer coding" 
              className="rounded-2xl shadow-2xl w-full max-w-md hover:scale-105 transition-transform duration-300"
            />
          </div>
        </div>
      </div>
    </section>
  );
};

export default About;
import { Button } from "@/components/ui/button";
import { Github, Linkedin, Mail } from "lucide-react";
import heroCoding from "@/assets/hero-coding.jpg";

const Hero = () => {
  return (
    <section className="relative min-h-screen flex items-center justify-center px-4 py-20 overflow-hidden">
      <div className="absolute inset-0 bg-gradient-to-br from-background via-background to-primary/10 z-0" />
      <div className="absolute inset-0 opacity-20 z-0">
        <img 
          src={heroCoding} 
          alt="Professional developer workspace" 
          className="w-full h-full object-cover"
        />
      </div>
      <div className="relative z-10 max-w-4xl mx-auto text-center space-y-8 animate-fade-in">
        <div className="space-y-4">
          <h1 className="text-5xl md:text-7xl font-bold tracking-tight">
            Hi, I'm <span className="bg-gradient-to-r from-primary to-accent bg-clip-text text-transparent">Your Name</span>
          </h1>
          <p className="text-xl md:text-2xl text-muted-foreground">
            Master of Computer Applications Student
          </p>
        </div>
        
        <p className="text-lg text-muted-foreground max-w-2xl mx-auto leading-relaxed">
          Passionate about software development and problem-solving. Currently pursuing MCA with a focus on 
          building efficient and scalable applications using modern technologies.
        </p>

        <div className="flex gap-4 justify-center flex-wrap">
          <Button size="lg" className="gap-2">
            <Mail className="h-4 w-4" />
            Contact Me
          </Button>
          <Button size="lg" variant="outline" className="gap-2">
            <Github className="h-4 w-4" />
            GitHub
          </Button>
          <Button size="lg" variant="outline" className="gap-2">
            <Linkedin className="h-4 w-4" />
            LinkedIn
          </Button>
        </div>
      </div>
    </section>
  );
};

export default Hero;
import { Card, CardContent } from "@/components/ui/card";
import { Code2, Database } from "lucide-react";
import codingPattern from "@/assets/coding-pattern.jpg";

const skills = [
  { name: "Python", level: "Intermediate", icon: Code2, color: "from-blue-500 to-cyan-500" },
  { name: "Java", level: "Intermediate", icon: Code2, color: "from-orange-500 to-red-500" },
  { name: "C", level: "Intermediate", icon: Code2, color: "from-purple-500 to-pink-500" },
  { name: "HTML", level: "Advanced", icon: Code2, color: "from-green-500 to-emerald-500" },
  { name: "CSS", level: "Advanced", icon: Code2, color: "from-indigo-500 to-blue-500" },
  { name: "SQL", level: "Intermediate", icon: Database, color: "from-yellow-500 to-orange-500" },
];

const Skills = () => {
  return (
    <section id="skills" className="relative py-20 px-4 overflow-hidden">
      <div className="absolute inset-0 opacity-5">
        <img 
          src={codingPattern} 
          alt="" 
          className="w-full h-full object-cover"
        />
      </div>
      <div className="relative z-10 max-w-6xl mx-auto">
        <h2 className="text-3xl md:text-4xl font-bold mb-12 text-center">Technical Skills</h2>
        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
          {skills.map((skill, index) => (
            <Card 
              key={skill.name} 
              className="group hover:shadow-lg transition-all duration-300 hover:-translate-y-1 border-2"
              style={{ animationDelay: `${index * 100}ms` }}
            >
              <CardContent className="p-6">
                <div className="flex items-center gap-4">
                  <div className={`p-3 rounded-lg bg-gradient-to-br ${skill.color}`}>
                    <skill.icon className="h-6 w-6 text-white" />
                  </div>
                  <div>
                    <h3 className="font-semibold text-lg">{skill.name}</h3>
                    <p className="text-sm text-muted-foreground">{skill.level}</p>
                  </div>
                </div>
              </CardContent>
            </Card>
          ))}
        </div>
      </div>
    </section>
  );
};

export default Skills;
