---
layout: project
type: project
image: img/react/react.png
title: "Next.js Personal Choice Website"
date: 2024
published: true
labels:
  - Next.js
  - GitHub
summary: "A website that I developed for ICS 314."
---

<img class="img-fluid" src="../img/react/react.png">

---

A simple webpage using Next.js that is based on the New York Times website. The links work and it was mainly a test to see Next.js capabilities.

---

### Features

#### Card Segments with Working Links

```cpp

<Card.Body>
  <a
    href="https://www.nytimes.com/2024/10/15/world/middleeast/us-israel-military-aid-gaza-improvements.html" 
    target="_blank"
    rel="noopener noreferrer"
    style={{ textDecoration: 'none', color: 'inherit' }}
  >
    <Card.Title className="fw-bold">
      U.S. Warns Israel to Increase Aid to Gaza or Face Consequences
    </Card.Title>
    <Card.Text>
      The warning was conveyed in a letter sent Sunday to two top Israeli officials that included 
      the possibility of a cutoff of U.S. military aid, officials said.
    </Card.Text>
    <p className="text-muted">6 MIN READ</p>
  </a>
</Card.Body>

```

#### Working date and time

```cpp

const LogoSection = () => {
  const [dateTime, setDateTime] = useState(new Date());

  useEffect(() => {
    const timer = setInterval(() => setDateTime(new Date()), 1000);
    return () => clearInterval(timer);
  }, []);
  
  return (
    <div>
      {dateTime.toLocaleString()}
    </div>
  );
};

```

#### Single drop down menu next.js doesnt allow for multiple

```cpp

const DropdownMenu = () => (
  <DropdownButton id="dropdown-basic-button" title="U.S." variant="light">
    {['Politics', 'New York', 'California', 'Education', 'Health'].map((item) => (
      <Dropdown.Item key={item}>{item}</Dropdown.Item>
    ))}
  </DropdownButton>
);

```