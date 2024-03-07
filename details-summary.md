# summary css 커스텀

        <details>
          <summary>summary</summary>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Blanditiis, est! Consequuntur porro quasi aliquam adipisci dolorum iusto dignissimos necessitatibus eveniet ea? A nemo voluptatum sit non tenetur labore beatae iste!</p>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat, voluptatum!</p>
        </details>


        <style>
          details {}
          details summary {padding: 20px; background-color: bisque; width: 500px; border: 1px solid bisque; list-style-image: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/3/right-arrow.svg);}
          details[open] > summary {list-style-image: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/9632/down-arrow.svg);}
          summary::-webkit-details-marker {background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/3/right-arrow.svg); color: transparent;}
          details[open] > summary::-webkit-details-marker {background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/9632/down-arrow.svg);}
          details p {border: 1px solid #000; width: 500px; padding: 20px; margin: 0;}
          details p:last-child {margin-top: -1px;}
        </style>
