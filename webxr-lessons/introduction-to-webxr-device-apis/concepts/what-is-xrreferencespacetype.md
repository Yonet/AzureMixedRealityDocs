# What is XRReferenceSpaceType?

XRReferenceSpaceType defines how much your user can move in you experience. 



<table>
  <thead>
    <tr>
      <th style="text-align:left">XRReferenceSpaceType</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left">Interface</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>bounded-floor</code>
      </td>
      <td style="text-align:left">Similar to the <code>local</code> type, except the user is not expected
        to move outside a predetermined boundary, given by the <a href="https://developer.mozilla.org/en-US/docs/Web/API/XRBoundedReferenceSpace/boundsGeometry"><code>boundsGeometry</code></a> in
        the returned object.</td>
      <td style="text-align:left"><a href="https://developer.mozilla.org/en-US/docs/Web/API/XRBoundedReferenceSpace"><code>XRBoundedReferenceSpace</code></a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>local</code>
      </td>
      <td style="text-align:left">
        <p>A tracking space whose native origin is located near the viewer&apos;s
          position at the time the session was created. The exact position depends
          on the underlying platform and implementation. The user isn&apos;t expected
          to move much if at all beyond their starting position, and tracking is
          optimized for this use case.</p>
        <p>For devices with six degrees of freedom (6DoF) tracking, the <code>local</code> reference
          space tries to keep the origin stable relative to the environment.</p>
      </td>
      <td style="text-align:left"><a href="https://developer.mozilla.org/en-US/docs/Web/API/XRReferenceSpace"><code>XRReferenceSpace</code></a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>local-floor</code>
      </td>
      <td style="text-align:left">Similar to the <code>local</code> type, except the starting position is
        placed in a safe location for the viewer to stand, where the value of the
        y axis is 0 at floor level. If that floor level isn&apos;t known, the
        <a
        href="https://developer.mozilla.org/en-US/docs/Glossary/user_agent">user agent</a>will estimate the floor level. If the estimated floor level
          is non-zero, the browser is expected to round it such a way as to avoid
          fingerprinting (likely to the nearest centimeter).</td>
      <td style="text-align:left"><a href="https://developer.mozilla.org/en-US/docs/Web/API/XRReferenceSpace"><code>XRReferenceSpace</code></a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>unbounded</code>
      </td>
      <td style="text-align:left">A tracking space which allows the user total freedom of movement, possibly
        over extremely long distances from their origin point. The viewer isn&apos;t
        tracked at all; tracking is optimized for stability around the user&apos;s
        current position, so the native origin may drift as needed to accommodate
        that need.</td>
      <td style="text-align:left"><a href="https://developer.mozilla.org/en-US/docs/Web/API/XRReferenceSpace"><code>XRReferenceSpace</code></a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>viewer</code>
      </td>
      <td style="text-align:left">A tracking space whose native origin tracks the viewer&apos;s position
        and orientation. This is used for environments in which the user can physically
        move around, and is supported by all instances of <a href="https://developer.mozilla.org/en-US/docs/Web/API/XRSession"><code>XRSession</code></a>,
        both immersive and inline, though it&apos;s most useful for inline sessions.
        It&apos;s particularly useful when determining the distance between the
        viewer and an input, or when working with offset spaces. Otherwise, typically,
        one of the other reference space types will be used more often.</td>
      <td
      style="text-align:left"><a href="https://developer.mozilla.org/en-US/docs/Web/API/XRReferenceSpace"><code>XRReferenceSpace</code></a>
        </td>
    </tr>
  </tbody>
</table>

