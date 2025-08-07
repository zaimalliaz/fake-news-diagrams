```jsx
const Box = ({ title, top, left, color, width = '160px', height = '50px' }) => (
  <div
    style={{
      position: 'absolute',
      top,
      left,
      width,
      height,
      display: 'flex',
      alignItems: 'center',
      justifyContent: 'center',
      fontSize: '15px',
      textAlign: 'center',
      backgroundColor: color || '#fff',
      border: '2px solid #2c3e50',
      borderRadius: '6px',
      fontWeight: '600',
      color: '#2c3e50',
      zIndex: 10,
      boxShadow: '0 2px 4px rgba(0,0,0,0.1)',
    }}
  >
    {title}
  </div>
);

const ArrowLabel = ({ text, x, y, rotation = 0 }) => (
  <text 
    x={x} 
    y={y} 
    fontSize="11px" 
    fontWeight="500"
    fill="#2c3e50"
    textAnchor="middle"
    dominantBaseline="middle"
    style={{
      backgroundColor: 'white',
      padding: '2px 5px',
      borderRadius: '3px',
      border: '1px solid #eee',
    }}
  >
    {text}
  </text>
);

export default function Diagram() {
  return (
    <div
      style={{
        position: 'relative',
        width: '100%',
        height: '700px',
        backgroundColor: '#f8f9fa',
        fontFamily: "'Georgia', 'Times New Roman', serif",
        padding: '30px',
        overflow: 'hidden',
      }}
    >
      {/* Header */}
      <div style={{ textAlign: 'center', marginBottom: '30px' }}>
        <div style={{ 
          fontSize: '12px', 
          fontWeight: 'bold', 
          color: '#c0392b',
          marginBottom: '5px',
          letterSpacing: '1px'
        }}>
          OFFICIAL: SENSITIVE
        </div>
        <h1 style={{
          fontSize: '22px',
          fontWeight: '600',
          margin: '0 auto',
          maxWidth: '800px',
          lineHeight: '1.4',
          color: '#2c3e50'
        }}>
          Manifestation of Belief and Idea in Thought:<br />
          How Disagreement is Negotiated
        </h1>
      </div>

      {/* Section Labels */}
      <div style={{ 
        position: 'absolute', 
        top: '110px', 
        left: '180px', 
        fontSize: '13px', 
        fontWeight: '500',
        color: '#7f8c8d',
        letterSpacing: '0.5px'
      }}>
        Articulation Process
      </div>
      <div style={{ 
        position: 'absolute', 
        top: '110px', 
        left: '450px', 
        fontSize: '13px', 
        fontWeight: '500',
        color: '#7f8c8d',
        letterSpacing: '0.5px'
      }}>
        Cultural & Societal Influences
      </div>
      <div style={{ 
        position: 'absolute', 
        top: '110px', 
        left: '720px', 
        fontSize: '13px', 
        fontWeight: '500',
        color: '#7f8c8d',
        letterSpacing: '0.5px'
      }}>
        Disagreement Effects
      </div>

      {/* Main Boxes */}
      <Box title="ARTICULATION" top="150px" left="180px" color="#e8f4f8" />
      <Box title="DISAGREEMENT" top="150px" left="700px" color="#f5f5f5" />
      <Box title="IDEAS" top="320px" left="180px" color="#f9e8e8" />
      <Box title="BELIEF" top="320px" left="700px" color="#e8f8f0" />
      <Box title="SOCIETY" top="490px" left="180px" color="#f0f8e8" />
      <Box title="CULTURE" top="490px" left="700px" color="#f0f8e8" />

      {/* SVG Arrows and Labels */}
      <svg
        style={{
          position: 'absolute',
          top: 0,
          left: 0,
          width: '100%',
          height: '100%',
          zIndex: 5,
        }}
      >
        <defs>
          <marker 
            id="arrow" 
            markerWidth="10" 
            markerHeight="10" 
            refX="9" 
            refY="3" 
            orient="auto"
          >
            <path d="M0,0 L0,6 L9,3 z" fill="#2c3e50" />
          </marker>
          <marker 
            id="dashed-arrow" 
            markerWidth="10" 
            markerHeight="10" 
            refX="9" 
            refY="3" 
            orient="auto"
          >
            <path d="M0,0 L0,6 L9,3 z" fill="#7f8c8d" />
          </marker>
        </defs>

        {/* ARTICULATION → IDEAS */}
        <line x1="260" y1="200" x2="260" y2="320" stroke="#2c3e50" strokeWidth="2" markerEnd="url(#arrow)" />
        <ArrowLabel text="Communicates" x="220" y="260" />

        {/* ARTICULATION → DISAGREEMENT */}
        <line x1="340" y1="175" x2="700" y2="175" stroke="#7f8c8d" strokeWidth="1.5" strokeDasharray="5,3" markerEnd="url(#dashed-arrow)" />
        <ArrowLabel text="Influences" x="520" y="165" />

        {/* ARTICULATION → BELIEF */}
        <line x1="340" y1="200" x2="700" y2="340" stroke="#7f8c8d" strokeWidth="1.5" strokeDasharray="5,3" markerEnd="url(#dashed-arrow)" />
        <ArrowLabel text="Influences" x="430" y="220" />

        {/* DISAGREEMENT → IDEAS */}
        <line x1="700" y1="200" x2="340" y2="320" stroke="#7f8c8d" strokeWidth="1.5" strokeDasharray="5,3" markerEnd="url(#dashed-arrow)" />
        <ArrowLabel text="Reflects" x="600" y="220" />

        {/* DISAGREEMENT → BELIEF */}
        <line x1="780" y1="200" x2="780" y2="320" stroke="#2c3e50" strokeWidth="2" markerEnd="url(#arrow)" />
        <ArrowLabel text="Refines" x="801" y="260" />

        {/* IDEAS → BELIEF */}
        <line x1="340" y1="340" x2="700" y2="340" stroke="#7f8c8d" strokeWidth="1.5" strokeDasharray="5,3" markerEnd="url(#dashed-arrow)" />
        <ArrowLabel text="Transforms" x="520" y="335" />

        {/* BELIEF → IDEAS */}
        <line x1="700" y1="360" x2="340" y2="360" stroke="#7f8c8d" strokeWidth="1.5" strokeDasharray="5,3" markerEnd="url(#dashed-arrow)" />
        <ArrowLabel text="Challenges" x="520" y="355" />

        {/* IDEAS → SOCIETY */}
        <line x1="260" y1="370" x2="260" y2="490" stroke="#2c3e50" strokeWidth="2" markerEnd="url(#arrow)" />
        <ArrowLabel text="Expresses" x="230" y="430" />

        {/* BELIEF → CULTURE */}
        <line x1="780" y1="370" x2="780" y2="490" stroke="#2c3e50" strokeWidth="2" markerEnd="url(#arrow)" />
        <ArrowLabel text="Reinforces" x="810" y="430" />

        {/* SOCIETY → CULTURE */}
        <line x1="340" y1="510" x2="700" y2="510" stroke="#7f8c8d" strokeWidth="1.5" strokeDasharray="5,3" markerEnd="url(#dashed-arrow)" />
        <ArrowLabel text="Shapes" x="520" y="505" />

        {/* CULTURE → SOCIETY */}
        <line x1="700" y1="530" x2="340" y2="530" stroke="#7f8c8d" strokeWidth="1.5" strokeDasharray="5,3" markerEnd="url(#dashed-arrow)" />
        <ArrowLabel text="Frames" x="520" y="525" />
      </svg>
    </div>
  );
}
