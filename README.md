import { motion } from "framer-motion";
import { Download } from "lucide-react";

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-gradient-to-br from-slate-900 via-slate-800 to-slate-900 text-white">
      {/* HERO SECTION */}
      <section className="relative h-screen flex items-center justify-center bg-[url('https://images.unsplash.com/photo-1503387762-592deb58ef4e')] bg-cover bg-center">
        <div className="absolute inset-0 bg-black/60" />
        <motion.div
          initial={{ opacity: 0, y: 40 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 1 }}
          className="relative z-10 text-center px-6"
        >
          <h1 className="text-5xl md:text-6xl font-bold">Dhiren Barhate</h1>
          <p className="mt-4 text-xl text-slate-200">
            Project Engineer | BIM & Digital Construction
          </p>
          <a
            href="/Dhiren_Barhate_CV.pdf"
            download
            className="inline-flex items-center gap-2 mt-8 px-6 py-3 bg-blue-600 hover:bg-blue-700 rounded-2xl text-lg shadow-lg"
          >
            <Download size={20} /> Download CV
          </a>
        </motion.div>
      </section>

      {/* SUMMARY */}
      <section className="max-w-6xl mx-auto px-6 py-20">
        <motion.h2 initial={{ opacity: 0 }} whileInView={{ opacity: 1 }} className="text-3xl font-semibold mb-6">Professional Summary</motion.h2>
        <p className="text-slate-300 text-lg leading-relaxed">
          Project Engineer with experience in construction execution, BIM-enabled coordination, and construction document management for residential and infrastructure projects. Skilled in interpreting drawings, models, and specifications, supporting RFI and submittal management, and identifying constructability risks early. Holds an MSc in Construction Management with exposure to BIM workflows and VDC practices.
        </p>
      </section>

      {/* PROJECT SLIDES */}
      <section className="bg-slate-800 py-20">
        <div className="max-w-6xl mx-auto px-6">
          <h2 className="text-3xl font-semibold mb-12">Key Projects</h2>
          <div className="grid md:grid-cols-3 gap-8">
            {["Bridge Restoration", "Sustainable Brick", "Water Treatment Plant"].map((project, i) => (
              <motion.div
                key={i}
                whileHover={{ scale: 1.05 }}
                className="bg-slate-900 rounded-2xl overflow-hidden shadow-xl"
              >
                <img
                  src="https://images.unsplash.com/photo-1504307651254-35680f356dfd"
                  alt={project}
                  className="h-48 w-full object-cover"
                />
                <div className="p-6">
                  <h3 className="text-xl font-semibold mb-2">{project}</h3>
                  <p className="text-slate-400 text-sm">
                    Design review, constructability analysis, BIM-supported coordination and execution planning.
                  </p>
                </div>
              </motion.div>
            ))}
          </div>
        </div>
      </section>

      {/* SKILLS */}
      <section className="max-w-6xl mx-auto px-6 py-20">
        <h2 className="text-3xl font-semibold mb-10">Core Skills</h2>
        <div className="grid md:grid-cols-4 gap-4">
          {["Project Engineering", "BIM Coordination", "RFI Management", "Submittals", "Constructability Review", "Change Management", "QA/QC", "AutoCAD", "Revit", "Navisworks", "BIM Collaborate", "MS Excel"].map((skill, i) => (
            <motion.div
              key={i}
              initial={{ opacity: 0, y: 20 }}
              whileInView={{ opacity: 1, y: 0 }}
              className="bg-slate-800 p-4 rounded-xl text-center"
            >
              {skill}
            </motion.div>
          ))}
        </div>
      </section>

      {/* FOOTER */}
      <footer className="bg-black/40 py-10 text-center text-slate-400">
        <p>Pune, India | +91-9359830776 | barhatedhiren123@gmail.com</p>
        <p className="mt-2">LinkedIn: linkedin.com/in/dhiren-barhate-80a78a147</p>
      </footer>
    </div>
  );
}
