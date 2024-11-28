import React from 'react';
import { 
  Code, 
  Database, 
  Server, 
  Monitor, 
  Cpu, 
  Terminal, 
  GitHub, 
  Linkedin, 
  Mail 
} from 'lucide-react';

const GithubProfile = () => {
  const skills = [
    { category: 'Programming Languages', 
      items: [
        { name: 'JavaScript', icon: Code, color: 'text-yellow-500' },
        { name: 'PHP', icon: Terminal, color: 'text-indigo-600' },
        { name: 'C', icon: Cpu, color: 'text-blue-600' },
        { name: 'C++', icon: Cpu, color: 'text-blue-800' },
        { name: 'C#', icon: Cpu, color: 'text-purple-600' }
      ]
    },
    { category: 'Frontend', 
      items: [
        { name: 'React', icon: Monitor, color: 'text-cyan-500' },
        { name: 'HTML5', icon: Code, color: 'text-orange-600' },
        { name: 'CSS3', icon: Code, color: 'text-blue-700' }
      ]
    },
    { category: 'Backend & DevOps', 
      items: [
        { name: 'Node.js', icon: Server, color: 'text-green-600' },
        { name: 'MongoDB', icon: Database, color: 'text-green-500' },
        { name: 'MySQL', icon: Database, color: 'text-blue-500' },
        { name: 'Docker', icon: Server, color: 'text-blue-600' },
        { name: '.NET', icon: Server, color: 'text-purple-500' }
      ]
    }
  ];

  const socialLinks = [
    { 
      name: 'GitHub', 
      icon: GitHub, 
      url: 'https://github.com/neptune2k21', 
      color: 'text-gray-800 hover:text-black' 
    },
    { 
      name: 'Email', 
      icon: Mail, 
      url: 'mailto:mamadoulcisse9236@gmail.com', 
      color: 'text-red-600 hover:text-red-800' 
    }
  ];

  return (
    <div className="min-h-screen bg-gray-50 text-gray-900 p-8">
      <div className="max-w-4xl mx-auto">
        {/* Header */}
        <div className="text-center mb-12">
          <h1 className="text-4xl font-bold mb-4 text-transparent bg-clip-text bg-gradient-to-r from-blue-600 to-cyan-500">
            Mamadou Lamine Cissé
          </h1>
          <p className="text-xl text-gray-600 max-w-xl mx-auto">
            Computer Science Student | Full-Stack Developer | Tech Enthusiast
          </p>
        </div>

        {/* About Me */}
        <section className="mb-12 bg-white shadow-lg rounded-lg p-8">
          <h2 className="text-2xl font-semibold mb-6 border-b pb-2">
            🚀 About Me
          </h2>
          <div className="grid md:grid-cols-2 gap-6">
            <div>
              <p className="text-gray-700">
                Passionate 2nd-year Computer Science student dedicated to developing modern, 
                high-performance applications. Constantly exploring new technologies 
                and pushing the boundaries of software development.
              </p>
            </div>
            <div className="space-y-2">
              <div className="flex items-center">
                <Code className="mr-2 text-blue-500" size={24} />
                <span>Innovative Problem Solver</span>
              </div>
              <div className="flex items-center">
                <Server className="mr-2 text-green-500" size={24} />
                <span>Full-Stack Development</span>
              </div>
              <div className="flex items-center">
                <Terminal className="mr-2 text-purple-500" size={24} />
                <span>Continuous Learning Mindset</span>
              </div>
            </div>
          </div>
        </section>

        {/* Skills */}
        <section className="mb-12">
          <h2 className="text-2xl font-semibold text-center mb-8">
            💻 Tech Skills
          </h2>
          <div className="grid md:grid-cols-3 gap-6">
            {skills.map((skillCategory, index) => (
              <div 
                key={index} 
                className="bg-white shadow-md rounded-lg p-6 transform transition hover:scale-105"
              >
                <h3 className="text-xl font-semibold mb-4 text-gray-700">
                  {skillCategory.category}
                </h3>
                <div className="space-y-3">
                  {skillCategory.items.map((skill, skillIndex) => (
                    <div 
                      key={skillIndex} 
                      className="flex items-center space-x-3 bg-gray-100 p-2 rounded-md"
                    >
                      <skill.icon className={`${skill.color}`} size={24} />
                      <span className="text-gray-800">{skill.name}</span>
                    </div>
                  ))}
                </div>
              </div>
            ))}
          </div>
        </section>

        {/* GitHub Stats */}
        <section className="mb-12 bg-white shadow-lg rounded-lg p-8">
          <h2 className="text-2xl font-semibold mb-6 text-center">
            📊 GitHub Statistics
          </h2>
          <div className="grid md:grid-cols-3 gap-6">
            <div className="text-center">
              <img 
                src="https://github-readme-stats.vercel.app/api/top-langs?username=neptune2k21&show_icons=true&locale=en&layout=compact&theme=transparent" 
                alt="Top Languages" 
                className="w-full rounded-lg shadow-md"
              />
            </div>
            <div className="text-center">
              <img 
                src="https://github-readme-stats.vercel.app/api?username=neptune2k21&show_icons=true&locale=en&theme=transparent" 
                alt="GitHub Stats" 
                className="w-full rounded-lg shadow-md"
              />
            </div>
            <div className="text-center">
              <img 
                src="https://github-readme-streak-stats.herokuapp.com/?user=neptune2k21&theme=transparent" 
                alt="GitHub Streak" 
                className="w-full rounded-lg shadow-md"
              />
            </div>
          </div>
        </section>

        {/* Contact */}
        <section className="text-center">
          <h2 className="text-2xl font-semibold mb-6">🤝 Let's Connect</h2>
          <div className="flex justify-center space-x-6">
            {socialLinks.map((link, index) => (
              <a 
                key={index} 
                href={link.url} 
                target="_blank" 
                rel="noopener noreferrer"
                className={`${link.color} transition-transform transform hover:scale-110`}
              >
                <link.icon size={36} />
              </a>
            ))}
          </div>
          <p className="mt-4 text-gray-600">
            Feel free to explore my projects or get in touch! 👋
          </p>
        </section>
      </div>
    </div>
  );
};

export default GithubProfile;
