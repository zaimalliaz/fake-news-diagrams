

const Box = ({ title, top, left, color }) => (
  <div
    style={{
      position: 'absolute',
      top,
      left,
      width: '140px',
      height: '40px',
      lineHeight: '40px',
      fontSize: '13px',
      textAlign: 'center',
      backgroundColor: color || '#fff',
      border: '2px solid black',
      borderRadius: '4px',
      fontWeight: 'bold',
      color: '#000',
    }}
  >
    {title}
  </div>
);

export default function Diagram() {
  return (
    <div
      id="diagram-container"
      style={{
        position: 'relative',
        width: '100%',
        height: '850px',
        backgroundColor: '#f7f7f7',
        fontFamily: 'Segoe UI, sans-serif',
        padding: '20px'
      }}
    >
      <h1 style={{
        textAlign: 'center',
        fontSize: '18px',
        fontWeight: 'bold',
        marginBottom: '20px',
        maxWidth: '800px',
        margin: '0 auto'
      }}>
        <span style={{ display: 'block' }}>OFFICIAL: SENSITIVE</span>
        Manifestation of Belief and Idea in Thought: How Disagreement is Negotiated
      </h1>

      {/* Context Labels */}
      <div style={{ position: 'absolute', top: '60px', left: '180px', fontSize: '11px', fontStyle: 'italic' }}>Articulation Process</div>
      <div style={{ position: 'absolute', top: '60px', left: '620px', fontSize: '11px', fontStyle: 'italic' }}>Disagreement Effects</div>
      <div style={{ position: 'absolute', top: '60px', left: '410px', fontSize: '11px', fontStyle: 'italic' }}>Cultural & Societal Influences</div>

      {/* Main Boxes */}
      <Box title="ARTICULATION" top="120px" left="200px" color="#bae0ff" />
      <Box title="DISAGREEMENT" top="120px" left="600px" color="#d3d3d3" />
      <Box title="IDEAS" top="270px" left="200px" color="#ffb6c1" />
      <Box title="BELIEF" top="270px" left="600px" color="#add8e6" />
      <Box title="SOCIETY" top="420px" left="200px" color="#e0f7fa" />
      <Box title="CULTURE" top="420px" left="600px" color="#e0f7fa" />

      {/* SVG Connectors */}
      <svg style={{ position: 'absolute', top: 0, left: 0, width: '100%', height: '100%' }}>
        <defs>
          <marker id="arrow" markerWidth="10" markerHeight="10" refX="5" refY="3" orient="auto" markerUnits="strokeWidth">
            <path d="M0,0 L0,6 L9,3 z" fill="#000" />
          </marker>
        </defs>

        {/* Communicates */}
        <line x1="270" y1="160" x2="270" y2="270" stroke="black" strokeWidth="1.5" markerEnd="url(#arrow)" />
        <text x="275" y="220" fontSize="10" fill="black">Communicates</text>

        {/* Expresses */}
        <line x1="270" y1="310" x2="270" y2="420" stroke="black" strokeWidth="1.5" markerEnd="url(#arrow)" />
        <text x="275" y="370" fontSize="10" fill="black">Expresses</text>

        {/* Shapes */}
        <line x1="270" y1="440" x2="620" y2="440" stroke="black" strokeWidth="1.5" strokeDasharray="4" markerEnd="url(#arrow)" />
        <text x="420" y="430" fontSize="10" fill="black">Shapes</text>

        {/* Reflects (Disagreement to Ideas) */}
        <line x1="600" y1="150" x2="270" y2="270" stroke="black" strokeWidth="1.5" strokeDasharray="4" markerEnd="url(#arrow)" />
        <text x="400" y="190" fontSize="10" fill="black">Reflects</text>

        {/* Refines */}
        <line x1="680" y1="160" x2="680" y2="270" stroke="black" strokeWidth="1.5" markerEnd="url(#arrow)" />
        <text x="685" y="220" fontSize="10" fill="black">Refines</text>

        {/* Reinforces */}
        <line x1="680" y1="310" x2="680" y2="420" stroke="black" strokeWidth="1.5" markerEnd="url(#arrow)" />
        <text x="685" y="370" fontSize="10" fill="black">Reinforces</text>

        {/* Transforms (IDEAS to BELIEF) */}
        <line x1="340" y1="290" x2="600" y2="290" stroke="black" strokeWidth="1.5" markerEnd="url(#arrow)" strokeDasharray="4" />
        <text x="450" y="280" fontSize="10" fill="black">Transforms</text>

        {/* Challenges (BELIEF to IDEAS) */}
        <line x1="600" y1="310" x2="340" y2="310" stroke="black" strokeWidth="1.5" markerEnd="url(#arrow)" strokeDasharray="4" />
        <text x="430" y="325" fontSize="10" fill="black">Challenges</text>
      </svg>

      {/* Footer Text */}
      <p style={{
        position: 'absolute',
        bottom: '10px',
        left: '50%',
        transform: 'translateX(-50%)',
        maxWidth: '750px',
        fontSize: '13px',
        textAlign: 'justify',
        padding: '10px',
        lineHeight: '1.4'
      }}>
        Navigating the Dance of Disagreement helps in mitigating the spread of fake news,
        emphasising the negotiation of disagreement and the psychological mechanisms involved.
        It helps curtail disinformation and misinformation, and address the psychological resistance
        to alternative viewpoints and arguments.
      </p>
    </div>
  );
}

